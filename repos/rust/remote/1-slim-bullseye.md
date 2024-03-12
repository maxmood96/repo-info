## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:559b0602185490f4de95e258407fea7ed166d6b2243775528f51d4fae2a06af9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:6efd48304f9e67612c60606ecd0fc122007148bd56f1fc08aec6302217bfbc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271547565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c400f84d497599ddf6a28e1a36252635be095e6810bcdd30137b9ad455828c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9a110c30f32996bbe446f451961dd74e2624594060a5e1c83a2e6468e97751`  
		Last Modified: Tue, 12 Mar 2024 01:57:19 GMT  
		Size: 240.1 MB (240125076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:e92e39ff9d37b8316835886d701dd52cda506bee33dff29928087d1a6b76bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109ef78260b5322a16b5761f6fdaf60b6a1056f176ee85de7d7f7b6420fd38c9`

```dockerfile
```

-	Layers:
	-	`sha256:cb06a86890ea268fbd990068fb4745f7ce09f06e800be46c02938a74d508b880`  
		Last Modified: Tue, 12 Mar 2024 01:57:15 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1256cf7777227b0566bcac759f3499434c32820c307539e9d2864182893d835d`  
		Last Modified: Tue, 12 Mar 2024 01:57:15 GMT  
		Size: 11.5 KB (11514 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:0142a51f3cda10c253bad2589e786dcdcd4d4ca9928853891de9562cc00dc982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285429609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3060387ce377e2c5d87fa6b3c9210362b72742dca3b06516b3aaff498a79612`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea968345cadeb2c9fb51ac82c986bf9065e24e1e59cf64104b3778b290fc38`  
		Last Modified: Mon, 11 Mar 2024 19:59:41 GMT  
		Size: 258.8 MB (258846937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:98b44c411d830a2fc4a3ea16b9cd269e06a5b2da1c63349d3ab3cf3a07d29d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f63a169a8113de50ec6a27d46671f43599b97bfe65c4e96b28284487e8c7d7`

```dockerfile
```

-	Layers:
	-	`sha256:79422569d14be226a5f3961ca8de7cad2c9de716a6b6758762142337a919cb29`  
		Last Modified: Mon, 11 Mar 2024 19:59:35 GMT  
		Size: 3.9 MB (3949600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e01ac66e267a4a6a59ed44b86b26f5911383e8a27838f8473e62bb6dee85b4b`  
		Last Modified: Mon, 11 Mar 2024 19:59:35 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:33e9664d1da4ef75a4d09f2d3534d12e950e0a3342f1aea82f8f583d34837f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335446412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9105e2d88ccfca21d95621fe4b3aefb2d406371e7ba84367a481d0dde8e3714e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85857aa5e40a2d9e0dfada91882836be4d4d3a202967ec96b5923254a609e1e8`  
		Last Modified: Mon, 11 Mar 2024 19:56:59 GMT  
		Size: 305.4 MB (305375335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:301fa4bfd1866bac7c48e069b99008bc1fe8ad54f3e2c597fecf5e4dec4a5dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910954df219906d4fb1a752fdb0f1cd4e56d7ac3ad763142df32fe52ab64666`

```dockerfile
```

-	Layers:
	-	`sha256:3e29416ef1fd0f987060b8dc1cf10aeaf596b1383df46919b47d5ae4a641f9ae`  
		Last Modified: Mon, 11 Mar 2024 19:56:52 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a97ed0a3a42c086ef9bcd1d30134b1ac21766f29d38a04dd7fc03ae5b8afbaa`  
		Last Modified: Mon, 11 Mar 2024 19:56:52 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b4f7fe6be5b28508e71cb98e306f205c93661ddb192e45d97736bc7f6bc10e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286676779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9e04e6c5e21e0e039c933b5ee69b1291fe997b21155006edc31bc29d62f573`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bab351a221f88bd92190fb476aac8bca9c7d65a5221dd61630014d2860586c0`  
		Last Modified: Tue, 12 Mar 2024 01:57:41 GMT  
		Size: 254.3 MB (254269190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07ede21243e4bd11e1ff97676630a78de7cfa874ca2fcc59160a3890e08b767f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c117934836dde810b5b6fe57558b3a0d76b04557a475ec662bb514bf2319b556`

```dockerfile
```

-	Layers:
	-	`sha256:3aac70965ade62a75e869949da5626a555c3a139320cf2cd2ea5d363b5f6fa66`  
		Last Modified: Tue, 12 Mar 2024 01:57:36 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e300a68b7e15cac09d41d332479a06c18b3e9dcdbf894bb18db039edd41d482d`  
		Last Modified: Tue, 12 Mar 2024 01:57:36 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:58194e3c33414cd3d85752837042a4108a246f622924238cf3a6d2162e9d5ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283689895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a86259013dbbe6a63d1ad0f12e6ea891767421ff29afa58e77fdf9999bc731c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd27a0abcc63b9b66130e750a577fa62a6db76be8c8f96abdaa26632a106d08`  
		Last Modified: Mon, 11 Mar 2024 20:08:34 GMT  
		Size: 248.4 MB (248392096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:51a649cbfaa6fee337d15f398a64394ca5a3578b09c9763797549f21efb1917c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5007cd20745e70478da297c3aa3a67bcac61f0f49839add0d9c4f40a0a6519`

```dockerfile
```

-	Layers:
	-	`sha256:10d9a0c29bc8748fe93eec9e22ca9d51bae20e54764d5d2f64d0f1fb655befc5`  
		Last Modified: Mon, 11 Mar 2024 20:08:28 GMT  
		Size: 4.1 MB (4100758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d4587c2b66b2153a8cc69c606762613c5a4245dc4d546ce673431d77a78b72`  
		Last Modified: Mon, 11 Mar 2024 20:08:28 GMT  
		Size: 11.4 KB (11385 bytes)  
		MIME: application/vnd.in-toto+json
