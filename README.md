# Build and Run helloworld  with Ruxgo

Here are two methods for building a helloworld application using the Ruxgo:

**Method 1**: Utilizing the Ruxgo's Package Management Tool

```bash
# Show the current support package list
ruxgo pkg -l

# Pull the helloworld and ruxos package
ruxgo pkg -p rux-helloworld
ruxgo pkg -p ruxos

# Build and Run
cd ruxos_pkg/rux-helloworld
ruxgo -b
ruxgo -r
```

**Note**: Since `rux-helloworld` needs to run on `ruxos`, you should also pull the `ruxos` locally. Also ensure that `ruxos` and the `rux-helloworld` package you fetched are in the same directory level. 

**Method 2**: Copying the Repository into the RuxOS Source Code

```bash
# Clone the Repository into the RuxOS Source Code
git clone https://github.com/syswonder/rux-helloworld ./apps/c/helloworld/

# Build and Run
cd ruxos/apps/c/helloworld
ruxgo -b
ruxgo -r
```

**Note**: Make sure you have the RuxOS source code already.