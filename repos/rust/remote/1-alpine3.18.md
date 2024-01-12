## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:9b3aae3c442e2023440a42f4897b888a0fcc78819bffbdf751582ec7467a2eda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:ec7440dfc11d747c1c22481a7ed5232b188f3cc77839ce4b4e9e9c20041db719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271819766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c4084bba29bcfbf1d879c97b84ade166ab90d654e685febae061f797f019b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2023 16:30:38 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6bacc066e07a23c0bef11b526d74a24bb497c4b4f35410fc596c9c93f1a8d5`  
		Last Modified: Fri, 12 Jan 2024 19:56:13 GMT  
		Size: 51.5 MB (51528301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2313384ac4b603d1c3c78b7bbeaf36cbabee3ae618261b7d6ed592cc3351e`  
		Last Modified: Fri, 12 Jan 2024 19:56:17 GMT  
		Size: 216.9 MB (216889043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:8df3def68677796ebea0ad38010e6541c5555b1581d8b3517d166c89d4b2ecfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.8 KB (599811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b601c7053be9e409b2df7c4a359e28bf40fbcbf284a66715af23da1994025244`

```dockerfile
```

-	Layers:
	-	`sha256:b93b6fc66645e17afb35f9978f2d39b31121f14427f5726dad4e85c5ff2e1614`  
		Last Modified: Fri, 12 Jan 2024 19:56:12 GMT  
		Size: 589.3 KB (589327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837d821f1140331badc2b2e90993ea0e37e6ea3a9dfad0f3c78437c9fd57ad63`  
		Last Modified: Fri, 12 Jan 2024 19:56:11 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ca2924c33d825e3b275ccd4b6310f4ce0a140921e6cea456758c0bf2347f12a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278052050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3ed3f96f8f52d6331a6f54517e9e476982e4391538e02d1798dab2168f98b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2023 16:30:38 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Dec 2023 16:30:38 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:30:38 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdcfe10a17d089515f9cb1689dbfbb36590136f89c5a3c4becf979879daa099`  
		Last Modified: Fri, 12 Jan 2024 20:57:56 GMT  
		Size: 46.1 MB (46066363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf19f4e78cd6458577269a77e55a37e81df0145901bb75b77ab0dbe76acbba4`  
		Last Modified: Fri, 12 Jan 2024 20:57:59 GMT  
		Size: 228.7 MB (228652654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:95c2441f7d7cd03d26e6d42e532689108ea32fa33c9a42dbcaede3707342425c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.0 KB (633007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c5cb371e95bdc25d4f9c2f00da26e92238204609e3ab306cd8e508a0576672`

```dockerfile
```

-	Layers:
	-	`sha256:ee1e621635503842b4cf4bc9f19689cccf28b66cf687cabdce083ce44356c78e`  
		Last Modified: Fri, 12 Jan 2024 20:57:55 GMT  
		Size: 622.7 KB (622679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fe9b9471a1837b86e2d07139733c6a0d343c434321bb753392048a29053be3`  
		Last Modified: Fri, 12 Jan 2024 20:57:54 GMT  
		Size: 10.3 KB (10328 bytes)  
		MIME: application/vnd.in-toto+json
