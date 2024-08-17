## `sapmachine:lts-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:51f57e7591bb64fc54b6d6f9930b2cc022b45146d1b9278c9ee541bc68eabdd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bb15ee4e3012e61201131130c55c975b575b02f5f98c62e22a29e0df984bfc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245301161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f84ea85f416f82db098d1deb2b861b3ea518dc9a40579d566276ee1ea2afb2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55ee8bc369f4913e2405af4e95a4d9b7e9ddec93024856d78227948f18106f`  
		Last Modified: Fri, 19 Jul 2024 17:59:13 GMT  
		Size: 215.6 MB (215596008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f239db9aa10947625281d2853f998cb55b772a27fbf198e6fb994ba9359dc0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d675810d9ba9e74579dc54b09b0a6e2add7380acd9fbe79c0ce8e76c926ab1`

```dockerfile
```

-	Layers:
	-	`sha256:7a0e2cadd798c693ba3552514dba3807c0fa28f042a39b98a7ea244e0dd85192`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 2.4 MB (2449605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571981ffa31842a5eb518786c1e2f28ee3d072beae123911268624a58a6beecf`  
		Last Modified: Fri, 19 Jul 2024 17:59:11 GMT  
		Size: 13.1 KB (13064 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e0235d94b201cdd5d18ac72df02f12037eca6b0a46dcce4e56329c24ff9446de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242544510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c2a0aa8867d0ff5d262acd1941e02e2992f31e1d2a4b019ea5edfeb831a35`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0702038986356c3440bf49ddb10e4b1c8337d5136aaf103ab8043f0dba6a3`  
		Last Modified: Sat, 17 Aug 2024 04:16:13 GMT  
		Size: 213.7 MB (213700824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca4dadc3a3ffbdc8dda65db9c74845ed2e5fa2f62088790597cb778be760e0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be48549f49df927dacec25eda2e5e0571ec2936214ee23615a090bebe4152023`

```dockerfile
```

-	Layers:
	-	`sha256:f4fe49919b873fc64988db2142c16bbf9bbacc3e70318fe69a580d0a50ef2b02`  
		Last Modified: Sat, 17 Aug 2024 04:16:09 GMT  
		Size: 2.5 MB (2450240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35a4ff2701aef7b6322b8804380a022cf0eb3d8bd29db4da1271fe7c178a8c9`  
		Last Modified: Sat, 17 Aug 2024 04:16:08 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5487d35b0b34fbdf412f694586b1f12b8159515c9e27d6d38df92a4cc57261fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251565744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35501eee086a67d2ffab39c0f3a69022d27507f3f4d76e45fff6a8fd9c9d3269`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b635f6eb6a60370f38c733b410c2c5c704b50b31485a59ebb304b4975e12d0`  
		Last Modified: Sat, 17 Aug 2024 02:46:41 GMT  
		Size: 217.1 MB (217058172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b9307dc54eb579dfe51c69fc40df176dc9673daed6c8127d745c72c7e0942478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486f6dae696c04e012c950a981b5cdaa57c382fb8f26a75141e77964f1d660f5`

```dockerfile
```

-	Layers:
	-	`sha256:251f3425df60f23b4d90b55f66e983e3fce51e32369a21aecbb785611f890f53`  
		Last Modified: Sat, 17 Aug 2024 02:46:35 GMT  
		Size: 2.5 MB (2451677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27fd18a9f035efde98cb8bc6a67f91e32db84db3a47bdfdc5e57074e7abfb751`  
		Last Modified: Sat, 17 Aug 2024 02:46:35 GMT  
		Size: 13.2 KB (13186 bytes)  
		MIME: application/vnd.in-toto+json
