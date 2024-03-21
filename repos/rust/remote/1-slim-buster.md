## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:d277fed352ff5d0ece628819514487a990bf38a3343925f3f8bcd24436f8db32
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

### `rust:1-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:8052db6c68465d833792856776728c6acf4f0026bdaedc470fc7da7c5247ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245517542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63251c8e701fa1b1ad292c537777e72570c2ead21f28ae095e239b9d80093620`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:45 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
# Tue, 12 Mar 2024 01:21:46 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6397fbd30dbd5a5b3b96e5c59c905ed829d5c625dd7e9e73dcca175ad575182e`  
		Last Modified: Thu, 21 Mar 2024 18:49:46 GMT  
		Size: 218.3 MB (218329238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:379780a0f7ea948d314b281da78f87985a9e71b2d66e540cea3a76d857a96b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1341fcd95b03a507386b10e69d83cec6acf8901340db6df20eadcd1f12fc3023`

```dockerfile
```

-	Layers:
	-	`sha256:4850755279929bf3f883d719d1ee6fd4401786fb644508ee0dffa6f9b0bfea89`  
		Last Modified: Thu, 21 Mar 2024 18:49:43 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82b4dbbe75907f963400de770ef42d163bc357ec49b2902ef47ef8fb13df68d`  
		Last Modified: Thu, 21 Mar 2024 18:49:42 GMT  
		Size: 11.1 KB (11112 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:299681bab6ffda8a54a897c4c2d269827b7c484350165f23485cc3389c61e361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264311999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5438c53a409645ee3c28f66d4b18104d78a7e01595c443640509e35c549a705d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:57 GMT
ADD file:87f5e14c74c217f7538860dd43d6b1910663955972cf5270e3d1a8254956878c in / 
# Tue, 12 Mar 2024 00:59:57 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f02c84b2c1c85cfdbae8bb78a52226f2b54d86f3eb2466ac3a81fc25ffde9eb`  
		Last Modified: Tue, 12 Mar 2024 01:05:07 GMT  
		Size: 22.8 MB (22795622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa847a8bd4cef3b03ab1a0610109d681a1c54abc61604de5e3ecd178dce5d7d`  
		Last Modified: Thu, 21 Mar 2024 18:53:57 GMT  
		Size: 241.5 MB (241516377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:9c367b2bd642f66036eaf520e9f8bdf722f301c6c845487f1215f5de50b0b2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3404129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60171eaf7e90c32f63d166d76f5958fbe162e68a70f58f1f1c656d57892b9c32`

```dockerfile
```

-	Layers:
	-	`sha256:27c45394066087e790495ff3dcd689bee38ab7352fcf5c51caaecb98c9d44266`  
		Last Modified: Thu, 21 Mar 2024 18:53:52 GMT  
		Size: 3.4 MB (3392947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c7f9deab01ec04dc61b4eef07783ef94b97a961456343552157ad8122391ff`  
		Last Modified: Thu, 21 Mar 2024 18:53:51 GMT  
		Size: 11.2 KB (11182 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3f8f862127da6664751414f9b398c2b2e77ae3214e8dd5967cb7d85879afc5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307811663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563e961818ab93ce481f69b2825be543795275817e123d1046dce1846ed14b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:05 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
# Tue, 12 Mar 2024 00:46:06 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2485cf6ef97bbfc549cf5b33cf3e08a2a987ff2a1df78b0691e240d0f3d18b2`  
		Last Modified: Thu, 21 Mar 2024 18:53:44 GMT  
		Size: 281.8 MB (281841074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:860a4fb3afa66945c847274b0dc2317f696a7ab8cb9dcf9877df5d1b3701899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da0386ee51a64286e1a28515814b722b910509e23c7d2328fb0b9fffb6f577`

```dockerfile
```

-	Layers:
	-	`sha256:db76dce0c26f8fa98b2a74ed1452012716ded03bc6cad7a595bcb9ee60bc5127`  
		Last Modified: Thu, 21 Mar 2024 18:53:38 GMT  
		Size: 3.6 MB (3574589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b9071ea2fac08a22829ca3e402934a926bdbd443215ad5384797bd9df8bb92`  
		Last Modified: Thu, 21 Mar 2024 18:53:38 GMT  
		Size: 11.1 KB (11122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:0be90744d8709f60011d83f79543e9f3874cfd5e91c50f0d4b7edf6b1b6e23fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264872988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd4bcda98b4c20f2a3177e70c3cafa480b21fc07efe4d319a6df614225d54b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:44 GMT
ADD file:c79a5b18bf34759ac9ea36615400037e5c793216013e88cec1fe6bda9664a062 in / 
# Tue, 12 Mar 2024 00:58:45 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:9e73dc674f1e3ae50c687941320c277d1320ed6eeda6f5f5ca3d1f70eee2bcff`  
		Last Modified: Tue, 12 Mar 2024 01:04:15 GMT  
		Size: 27.8 MB (27846708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0442460c1f5b9d122e1bce53f97e6975f2ed3f6310ba1a74cd943431390b57`  
		Last Modified: Thu, 21 Mar 2024 18:49:52 GMT  
		Size: 237.0 MB (237026280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:d88fa74e11e560b09ad0739be43f3cfa7f72b5124d58073aea83ea4122acf101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6f8f0aad96a4a66664efe65df4eb4335fdfbb5588c11f968a7fffe60a90d0f`

```dockerfile
```

-	Layers:
	-	`sha256:dd3a0b64ffd5d75a64381d787fe808d39aeabd08c7242ea595e070f3fad3c128`  
		Last Modified: Thu, 21 Mar 2024 18:49:47 GMT  
		Size: 3.6 MB (3591922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3de871eb4bf3c56ba9933d4f85483ce2c6472ce48a74619f887a7aeb76b568`  
		Last Modified: Thu, 21 Mar 2024 18:49:47 GMT  
		Size: 11.1 KB (11082 bytes)  
		MIME: application/vnd.in-toto+json
