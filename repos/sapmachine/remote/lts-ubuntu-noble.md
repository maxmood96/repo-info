## `sapmachine:lts-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3ce464fc9303027e6d1129e4a4488c64bc3845cf3db20532a5562bbb0305fed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7bdb926b363b6c74185f10fee7fbf5eb3de8bed31e7ee9e798a4be82e0dfc1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244784718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da63820a7dfb05ba3ecfa4a365703b7aa413dbae8912df3581a9352efd8ae267`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70df4abdc61489114701bb0d41f48ef316750e143da8798265da1d0891f783e3`  
		Last Modified: Tue, 04 Feb 2025 04:49:19 GMT  
		Size: 215.0 MB (215030428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f64a3d9b291bc82928cd19f5713455b9bd6e663252654fc2f65494ab0ec49a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f796f8436acac09e8f30ab856764fa2dc4f6ba111e6c447621124f7ee957689`

```dockerfile
```

-	Layers:
	-	`sha256:6c053f5c27eec3b12a58ebd2d9bb19d5d62402051712321bd7ec63b41bdf6838`  
		Last Modified: Tue, 04 Feb 2025 04:49:14 GMT  
		Size: 2.5 MB (2476392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8577f437c6a5bd6bdd51f5993c015ad5805604900dec141ccac72b910cd979e6`  
		Last Modified: Tue, 04 Feb 2025 04:49:14 GMT  
		Size: 13.3 KB (13318 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:036ec684b972cea186b48f935b55de28615115fc85f9e949455c6faa85928f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242175645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2987f58325fa8eff02e2a9e5e9db71bef0df281aabf881a35c85e34bc8bf84a9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19c229e63b62d60c56ac00bc3ed914323d95d6ac32ce83864ec017892c77fb5`  
		Last Modified: Tue, 04 Feb 2025 15:25:48 GMT  
		Size: 213.3 MB (213282047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52d99afa147f3531eed8a416b3fcc33a984707af9f64ffcf93982a34522e25c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2490619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa70bc44cefee8a6e2723cea53d6d17711b7127cfe27f50ade42d7941159edc`

```dockerfile
```

-	Layers:
	-	`sha256:743fb64faf6b1bdf9f76c087c39d683b8dcc317919604620e03ec89e991b5d52`  
		Last Modified: Tue, 04 Feb 2025 15:25:43 GMT  
		Size: 2.5 MB (2477028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e655863a60af3fb9c67d5758c8b27d3164c62348c7d9ef577a38746d398762`  
		Last Modified: Tue, 04 Feb 2025 15:25:43 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4205ab1ee3bf307b3c6bcea56d7209f66601102e48eaa8f6b68a196eb9ea8b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250838991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f173dacf0e96a51bd2f0f106b3847cbbbe75285c3c2e67a1e0896cba2502e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1d13b1101e75e47c344060f6963d384a4468b3d136333d805d07594da6b4d6`  
		Last Modified: Tue, 04 Feb 2025 14:34:21 GMT  
		Size: 216.4 MB (216449167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:84f39798d90382dd2e6a49929e54e9b7e7636fefa42c0c6c7cbe0fb3758f0e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2491916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca453fc9d406eeda16474899a704cb6351de9c46057cd1f461be2c5bf9a73568`

```dockerfile
```

-	Layers:
	-	`sha256:a1106f2eeadb6af4f60ecc7a0583e58e98483fef397a0b690e10b920e786db8a`  
		Last Modified: Tue, 04 Feb 2025 14:34:16 GMT  
		Size: 2.5 MB (2478469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a845818522f575dc52d454b2098f2ae5a0b8fdfd01894f7ce861d1a4a12f0af`  
		Last Modified: Tue, 04 Feb 2025 14:34:15 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
