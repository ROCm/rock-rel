# rockrel

Contains all the code for [TheRock](https://github.com/rocm/therock) releases. The name of this repo has been shortened to workaround this [known Windows path issue](https://github.com/ROCm/rocm-libraries/issues/2096).

## Prereleases

This provides a brief overview on how to install prereleases triggered with the workflows in this repository.
For general and more detailed information on releases, see [RELEASES](https://github.com/ROCm/TheRock/blob/main/RELEASES.md).

### Installing ROCm Python packages

To install ROCm and PyTorch Python packages, use `pip` with the `--index-url` option pointing to prereleases index page for your GPU architecture.
The packages are published to GPU-architecture-specific index pages.

| Product Name        | GFX Target | GFX Family   | Release Index                                      |
| --------------------| ---------- | ------------ | -------------------------------------------------- |
| MI300A/MI300X       | gfx942     | gfx94X-dcgpu | https://rocm.prereleases.amd.com/whl/gfx94X-dcgpu/ |
| MI350X/MI355X       | gfx950     | gfx950-dcgpu | https://rocm.prereleases.amd.com/whl/gfx950-dcgpu/ |
| AMD Strix Halo iGPU | gfx1151    | gfx1151      | https://rocm.prereleases.amd.com/whl/gfx1151/      |

Install instructions:
```bash
python -m pip install --index-url ${Release_Index} "rocm[libraries,devel]"
```

For more detailed instructions see TheRock's instructions on [installing releases using pip
](https://github.com/ROCm/TheRock/blob/main/RELEASES.md#installing-releases-using-pip).


### Installing from tarballs

Prerelease tarballs can be downloaded from https://rocm.prereleases.amd.com/tarball/.

After downloading, simply extract the release tarball into place:

```bash
mkdir therock-tarball && cd therock-tarball
# For example...
wget https://rocm.prereleases.amd.com/tarball/therock-dist-linux-gfx1151-7.9.0rc1.tar.gz

mkdir install
tar -xf *.tar.gz -C install
```
