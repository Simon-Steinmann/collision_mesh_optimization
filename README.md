# collision_mesh_optimization
A script that converts high detail visual meshes into a convex decomposition using v-hacd. Easily convert every mesh file in a directory or directory structure. 
Automatically extract visual meshes from a urdf file and generate a new urdf file with optimized collisions.


7

## Install

### From Sources

```
git clone https://github.com/Simon-Steinmann/collision_mesh_optimization.git
cd urdf2webots
pip install -r requirements.txt
```

## Usage

```
python collision_mesh_optimization_pybullet.py --input=example/UR5e.urdf 
```

## Arguments

```
Options:
  -h, --help         show this help message and exit
  --input=INPATH     Specifies the proto file, or a directory. Converts all
                     .proto files, if it is a directory.
  --outPath=OUTPATH  Where converted obj file should be placed.  Only use for
                     converting mesh files in a directory. It will place all
                     converted files in the outPath,  ignoring any further
                     recursive folder structure.
  --type=EXT         The file extensions to convert, if --input is a
                     directory. Can be list --type=".dae .stl .obj .urdf". If
                     defining multiple file extensions, make sure you surround
                     them by quotation marks and seperate them by spaces, as
                     shown in the example.
  --replace          If set, will replace .urdf  files instead of creating a
                     new "<filename>_optimized.urdf". This will turn the
                     --backup option  on.
  --backup           If set, will create a backup  of the "--input" directory
                     next to it.

```