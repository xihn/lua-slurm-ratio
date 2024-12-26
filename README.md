# lua-slurm-ratio
lua version of slurm cpu/gpu enforcer plugin

- To build this, first ensure slurm has been built with lua enabled. This requires 
the `lua` package and `lua-devel` package to be installed before `./configure` is ran.


- After simply place `job_submit.lua` in the same directory as `slurm.conf` (usually `/etc/slurm`). Then
modify `slurm.conf` to have `JobSubmitPlugins=lua`. Other plugins can come before or after ex, `JobSubmitPlugins=lua,plugin1,plugin2,`

- To customize simply edit the `.lua` file and reload `slurmctld`. 
