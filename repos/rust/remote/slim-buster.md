## `rust:slim-buster`

```console
$ docker pull rust@sha256:ec44c14c43cf551f6f442dee9982220c89c5fe3db9bca21dc38bc6b795b47145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:3b12fceaaa699c6ee20088f72c8e9f485165bb2af4f6fc744f9cec2afc8a3fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249874180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d21ad89a00374b10e1d9d7a48b251abd36fecc4f56945d76b795155bfa17c59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Dec 2023 16:30:38 GMT
ADD file:a857ebb18123e76fc79a7d720dfdcc496ba12a79af323564b965627d399a5b04 in / 
# Thu, 28 Dec 2023 16:30:38 GMT
CMD ["bash"]
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b992ca815489079dcc6d19cf381c63d057e1b924edd453734f694be5ee23dfd9`  
		Last Modified: Wed, 31 Jan 2024 22:41:30 GMT  
		Size: 27.2 MB (27188593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef231b22bae7d8e389d218e8d3b83a7cc3486a11a614de69e44b044cbf1553c`  
		Last Modified: Thu, 01 Feb 2024 00:08:23 GMT  
		Size: 222.7 MB (222685587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:330cee707ac9184f646737a842d825addef06d9ef2359b567c982730fd4572ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa00386d1d8eaee61f4fb2cb7760f618d41be78914d65e0a09f89ffb21d238d`

```dockerfile
```

-	Layers:
	-	`sha256:8dbc8511f9141c7eca4ba02efe2db287e472625ed478ee9c99b63dcd7ddc2391`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 3.1 MB (3116231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4028ab079bc081356d456db1ac6f66cc3b6c0a3b87b1292af58850decc37ffd3`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 11.1 KB (11112 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:639da31480f7ced50c0a10946fcb09bb53d74a779f706b17631f767028cd6d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270640847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7865c57ab0d7171f2b3f4cd134e5d7a5e50de6e16d6329ab2a01676e22d83375`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Dec 2023 16:30:38 GMT
ADD file:34e8fc4544a9986a7bf091ba5d31dbe51ee7c3c403fc9de427ca8944fe91298f in / 
# Thu, 28 Dec 2023 16:30:38 GMT
CMD ["bash"]
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:342befe29912bb1e1d01bf5c9c9e8e50b3a65a92b7f2b1d90c33a723259aae09`  
		Last Modified: Wed, 31 Jan 2024 22:50:19 GMT  
		Size: 22.8 MB (22795569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6246afdef8531aa7eb162d2e7341679b626c03b95f040d30abf9c2ef5ed9b3`  
		Last Modified: Fri, 02 Feb 2024 12:42:51 GMT  
		Size: 247.8 MB (247845278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:2b652e5b087b1dd13725d1c105ad0296ae96bdd7ac1b65b89a2b8fdade833e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a9c102465e4fc5a93bd2da40007c9b643c429a0bc54668837f1dc72ddbcaf3`

```dockerfile
```

-	Layers:
	-	`sha256:7744399218523e9da86aebaeff7402317204258820c1bede20b4e0a220c1f979`  
		Last Modified: Fri, 02 Feb 2024 12:42:46 GMT  
		Size: 2.9 MB (2948473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e333d431ac6b13e0180ec2be106285ac1d71b0d9cb6e81f0aa507784a732f8b`  
		Last Modified: Fri, 02 Feb 2024 12:42:45 GMT  
		Size: 11.0 KB (11015 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d1ea5e9cbf897e4ec1a174615bd488d1a88135ca53426364d075d5585248da72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314129167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f7a14b4688b2fc2f1b5bb66003ec1f412a16cd9947f604facbd272e7b25d6c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Dec 2023 16:30:38 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
# Thu, 28 Dec 2023 16:30:38 GMT
CMD ["bash"]
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5b4e7fc16bb39b801fd81d1e7d20ced14554939d8e6e6e41dc078ab49ba9a9`  
		Last Modified: Thu, 01 Feb 2024 21:34:17 GMT  
		Size: 288.2 MB (288158940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:dc2f25180ef40f8e80fc048000552fefc1d0747a8aed5947a22ff2233578d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3117644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae83476f5014a701d5b1cd5496d80ddbe8a2911e467c6e57632acf19b97426ce`

```dockerfile
```

-	Layers:
	-	`sha256:b0728409f140f4f54f67d2734a23904a98b399d70aa35e989625577bf38d37ca`  
		Last Modified: Thu, 01 Feb 2024 21:34:11 GMT  
		Size: 3.1 MB (3106689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f0728766e4b6ce84ee4aaa136b265cb29eb26c4cca93d75cbd031f8ddc32e5`  
		Last Modified: Thu, 01 Feb 2024 21:34:10 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; 386

```console
$ docker pull rust@sha256:71346fc3ede05cef194ecae4ca2a0ad4e2ba0f9084ed12ffc1d2f1c0cfd9ed14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268701618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102d970cb8ea02fc2c933c32bfe5075baa14eb7d8630d9edd077cbab9e5a704f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 28 Dec 2023 16:30:38 GMT
ADD file:08f96b15b2da153843e0da5de223845c3e2687e03502857416effec0f1070da2 in / 
# Thu, 28 Dec 2023 16:30:38 GMT
CMD ["bash"]
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d96589ec9f6e89924970de1915516d7b8a4e8fe3da0fd37bda398d2d3ae5b529`  
		Last Modified: Wed, 31 Jan 2024 22:45:26 GMT  
		Size: 27.8 MB (27846800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a69e2295f33c6ce5b2dab260e4f5d7e6d149364045924ad9b0ff02d8fcca8e`  
		Last Modified: Thu, 01 Feb 2024 00:08:47 GMT  
		Size: 240.9 MB (240854818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:ae9670bf7ded7af5bd6caf4651e15cee14d429a98031a6ea8431821dd858d4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f069fb88d6658c42e1f7209f3d69a0c7e14046eb5d3674e7ae45ba93cd71d8f`

```dockerfile
```

-	Layers:
	-	`sha256:9d13279a4a812cd604f0d1e9e805ddb4240a41a1d6d34bda2d0ea7fbea795c22`  
		Last Modified: Thu, 01 Feb 2024 00:08:40 GMT  
		Size: 3.1 MB (3120948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0f77613cf0bf93e70685e1c8dec855a6aaad3c99d8f5bbbc35d33d093041e1`  
		Last Modified: Thu, 01 Feb 2024 00:08:40 GMT  
		Size: 11.1 KB (11081 bytes)  
		MIME: application/vnd.in-toto+json
