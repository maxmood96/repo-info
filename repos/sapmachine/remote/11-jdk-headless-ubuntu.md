## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:afe3d06a7541662d8be14766522317341baa7d677320ca77ce0b33c94d0e78fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e99ec33939f0620c84d5318fc4f590d7ee00140013738a7b71702f7665a49a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229850875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d16af86697569f142f81ed905a54d733203e247306b230f953a45540910889a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1ed2853ce3472d7bd2df028f32cb4800dfdad324d6a9195a1cdd37fe93f04f`  
		Last Modified: Tue, 12 Aug 2025 22:29:33 GMT  
		Size: 200.1 MB (200127660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:148fd5a85a334edc4facfc4211a84f27ddbb61d9495b35ccc3b3c24120352f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d546c5cec0ecf68049ac90174452031d02adbc58ad451c7d37a8f3d01a5b3d74`

```dockerfile
```

-	Layers:
	-	`sha256:fa0386d37d86411bb2fa8e3f9d4be6f8b8ddfa53d18c30cebb783659a8df9999`  
		Last Modified: Tue, 12 Aug 2025 21:04:21 GMT  
		Size: 2.4 MB (2367208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ab7ed6d7990e3cd6240457f736b94fa41072b7b3afefbc021dc3f429bc334b`  
		Last Modified: Tue, 12 Aug 2025 21:04:21 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json
