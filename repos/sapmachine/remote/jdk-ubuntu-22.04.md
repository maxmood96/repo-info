## `sapmachine:jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0fa01b126914c4e24e61facddb0a54eff49f8a511a905c8fed25fd96f866a485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cb72d52e6da5b85fdb8c59a2ef9d02ba159d6d30273c3a478f3f827939b95939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242763574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591f825faba27799b9284f5240fdf07a789402928b5722fb26b445c0e510c0d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8895c1cd7d6b4056fb945937b74edab60d7ebc7f030e8e795b29462b3a103f92`  
		Last Modified: Fri, 19 Jul 2024 17:59:23 GMT  
		Size: 213.2 MB (213229519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8154a854ff56c8facadc3bd453d95033920f4e3d351403474ded98c22c0e343b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997207c8565ec49f7026b70eb4daac5290feb83ed6b6a4e049c8ec5d5d94c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:e4c3a664f3654d8a2b41a018fa5ad323f225a811bf7de03dbf6fd3a2811599a7`  
		Last Modified: Fri, 19 Jul 2024 17:59:20 GMT  
		Size: 2.5 MB (2475629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa7a5a37ee7e83c22d75f267623f37078125d01c412814b59ae5b11f9655097`  
		Last Modified: Fri, 19 Jul 2024 17:59:20 GMT  
		Size: 11.2 KB (11159 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7bda4d8237bfbe563d08f1096912d1a520084c1e61e459a6b0a4567650902cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238532771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f7d51daad3da728eb6dde1f5abe78235ef8b0ed3bd767d26738c11fa5e2e6c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e4032fd778681091dda16ec4ff545d5a0a55a73b901de9c28c151e1a1de818`  
		Last Modified: Sat, 17 Aug 2024 04:07:59 GMT  
		Size: 211.2 MB (211174088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5a566ccb4edaea0397d5d3515942e54f06f682cffc7c8d7b7ff1f851b52c0cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a71cfa5e359e59ef39d2a97970bb36d683b0a0962caf4b7ba4bec299eeb272`

```dockerfile
```

-	Layers:
	-	`sha256:feef9da764d522d0d06172b90c5ae9d74cc6d60bcf6d42aa052f773d04629dea`  
		Last Modified: Sat, 17 Aug 2024 04:07:55 GMT  
		Size: 2.5 MB (2474774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2864acbb66bd2b5796b288b56b37915eb04365107dae76288c143c6c157d29`  
		Last Modified: Sat, 17 Aug 2024 04:07:54 GMT  
		Size: 11.6 KB (11556 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:14a51efd043c7fc9d6d34cff8ec6bcb11caa1a8b4b1af063e3cb90332ebf632b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248777356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fb94a94dede79f0ca179c7cf0af99aef333b5f7c809378a5b5b00b0a379a1e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e572244fda177a481ac7ec887a6503032813c8f1991fec5aedb12edcfed8f51`  
		Last Modified: Sat, 17 Aug 2024 02:32:27 GMT  
		Size: 214.3 MB (214313178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f25aac6427e64d6b155a356355c59f49f5dcc1b58370413e2c734353a707f03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b66587746c12f4be069c57086665b4555660203c5949d4ece84c1c4753d2054`

```dockerfile
```

-	Layers:
	-	`sha256:b7d03415b42d6234d4a6007e324719cd2336d8634f593a9ee7162347bbab5244`  
		Last Modified: Sat, 17 Aug 2024 02:32:22 GMT  
		Size: 2.5 MB (2477088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338b5017f6dfffd1713d6854c12ccde5098a329d51e0307ff2794872ae56c6d7`  
		Last Modified: Sat, 17 Aug 2024 02:32:21 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json
