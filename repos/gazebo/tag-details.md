<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gazebo`

-	[`gazebo:gzserver11`](#gazebogzserver11)
-	[`gazebo:gzserver11-focal`](#gazebogzserver11-focal)
-	[`gazebo:latest`](#gazebolatest)
-	[`gazebo:libgazebo11`](#gazebolibgazebo11)
-	[`gazebo:libgazebo11-focal`](#gazebolibgazebo11-focal)

## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:ba7ffb8351af9e53aaef720fd86b5cbd39c638252ba3f3c9e8caace476325168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:97dfc0536447c8210e0d6388de059b9fd147d8444898ea31388d0fce823843c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8dbdfd1d82aad6029f6af5f59c78a3e324799ef69954cbbbf68a090001bbb82`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b27724939102ee35a9cdb48f34f5216667c81055955817b5cbbc269506bd1`  
		Size: 1.2 MB (1198847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fb44c058ddabcd4051befdffe65128238e5ec5036d38d25a65d857c1c0f28`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 5.4 MB (5361907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef3641eabd1611f862c208ee8576714e8a0a0253ccd0de885409f3f7e2e5676`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5384edf40a924ba3b6e4ebea240776edf6ea3cff04a008b1c2ab82791b7dec37`  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5c66f313291a95c156136e84c6a59e3ed3fd2443298d634c66303bf2a69e`  
		Last Modified: Mon, 09 Dec 2024 19:29:19 GMT  
		Size: 278.1 MB (278067567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d712a32f72d4975eb3825b3bed247e3f30513bd2d50f68734ef3d725fc7a99`  
		Last Modified: Mon, 09 Dec 2024 19:29:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11` - unknown; unknown

```console
$ docker pull gazebo@sha256:68b68e3662142ed7fe01ff75a39dbd2abf5a0748276249e7e771338dac0b0ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2f3d45503c32cb44eda593a3a461e0e03032f2c9c1d95bdeb36536083cae1e`

```dockerfile
```

-	Layers:
	-	`sha256:b2fd4c240b53351c78a6d3e62fcf076d57e4b54a3dc860ccd65a24304f3de5fc`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 6.6 MB (6604704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c9fac0b45648de2078dce3fe4fb810aa11491044ff7d74d0824832f6592d5e`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 16.4 KB (16355 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:ba7ffb8351af9e53aaef720fd86b5cbd39c638252ba3f3c9e8caace476325168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:97dfc0536447c8210e0d6388de059b9fd147d8444898ea31388d0fce823843c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8dbdfd1d82aad6029f6af5f59c78a3e324799ef69954cbbbf68a090001bbb82`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b27724939102ee35a9cdb48f34f5216667c81055955817b5cbbc269506bd1`  
		Size: 1.2 MB (1198847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fb44c058ddabcd4051befdffe65128238e5ec5036d38d25a65d857c1c0f28`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 5.4 MB (5361907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef3641eabd1611f862c208ee8576714e8a0a0253ccd0de885409f3f7e2e5676`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5384edf40a924ba3b6e4ebea240776edf6ea3cff04a008b1c2ab82791b7dec37`  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5c66f313291a95c156136e84c6a59e3ed3fd2443298d634c66303bf2a69e`  
		Last Modified: Mon, 09 Dec 2024 19:29:19 GMT  
		Size: 278.1 MB (278067567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d712a32f72d4975eb3825b3bed247e3f30513bd2d50f68734ef3d725fc7a99`  
		Last Modified: Mon, 09 Dec 2024 19:29:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:68b68e3662142ed7fe01ff75a39dbd2abf5a0748276249e7e771338dac0b0ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2f3d45503c32cb44eda593a3a461e0e03032f2c9c1d95bdeb36536083cae1e`

```dockerfile
```

-	Layers:
	-	`sha256:b2fd4c240b53351c78a6d3e62fcf076d57e4b54a3dc860ccd65a24304f3de5fc`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 6.6 MB (6604704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c9fac0b45648de2078dce3fe4fb810aa11491044ff7d74d0824832f6592d5e`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 16.4 KB (16355 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:latest`

```console
$ docker pull gazebo@sha256:4c294e47eb3752542b824618f8e95835909e27dfa14fa0b39f6410647d201da8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:3eea476332ca8c66ec98ca233191dd532eda7bea616f5a110fd8707f454b6df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609309801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0a27d0cf973beeeefbf7f38f32193c9cbbfe9e005372687d6a0fbf2e3cbaac`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b27724939102ee35a9cdb48f34f5216667c81055955817b5cbbc269506bd1`  
		Size: 1.2 MB (1198847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fb44c058ddabcd4051befdffe65128238e5ec5036d38d25a65d857c1c0f28`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 5.4 MB (5361907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef3641eabd1611f862c208ee8576714e8a0a0253ccd0de885409f3f7e2e5676`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5384edf40a924ba3b6e4ebea240776edf6ea3cff04a008b1c2ab82791b7dec37`  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5c66f313291a95c156136e84c6a59e3ed3fd2443298d634c66303bf2a69e`  
		Last Modified: Mon, 09 Dec 2024 19:29:19 GMT  
		Size: 278.1 MB (278067567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d712a32f72d4975eb3825b3bed247e3f30513bd2d50f68734ef3d725fc7a99`  
		Last Modified: Mon, 09 Dec 2024 19:29:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3050ffc3c19773a71bc3b1026cfc174ec32b3a97b6dd42f8ac2d6d3a95d64ca3`  
		Size: 297.2 MB (297168489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:latest` - unknown; unknown

```console
$ docker pull gazebo@sha256:5e456cfb80f91f5d184b9a016c089e378e268ff233ecfd93373ccf9b99e7af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37550374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4db618f5c3f4aafdd64ac2bb53af5858f584fbaa8cc3bc52dd1f039e41eb0c`

```dockerfile
```

-	Layers:
	-	`sha256:f13305cf555b2104abb7d8a0782217856fcd51f2b18e354ea105c5e5c373f6dd`  
		Last Modified: Mon, 09 Dec 2024 20:39:35 GMT  
		Size: 37.5 MB (37541712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a781552e8708b7f1ff4f52aa3cefb93f05dc179ea71dc170313789b30fb98e9f`  
		Last Modified: Mon, 09 Dec 2024 20:39:31 GMT  
		Size: 8.7 KB (8662 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:4c294e47eb3752542b824618f8e95835909e27dfa14fa0b39f6410647d201da8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:3eea476332ca8c66ec98ca233191dd532eda7bea616f5a110fd8707f454b6df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609309801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0a27d0cf973beeeefbf7f38f32193c9cbbfe9e005372687d6a0fbf2e3cbaac`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b27724939102ee35a9cdb48f34f5216667c81055955817b5cbbc269506bd1`  
		Size: 1.2 MB (1198847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fb44c058ddabcd4051befdffe65128238e5ec5036d38d25a65d857c1c0f28`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 5.4 MB (5361907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef3641eabd1611f862c208ee8576714e8a0a0253ccd0de885409f3f7e2e5676`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5384edf40a924ba3b6e4ebea240776edf6ea3cff04a008b1c2ab82791b7dec37`  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5c66f313291a95c156136e84c6a59e3ed3fd2443298d634c66303bf2a69e`  
		Last Modified: Mon, 09 Dec 2024 19:29:19 GMT  
		Size: 278.1 MB (278067567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d712a32f72d4975eb3825b3bed247e3f30513bd2d50f68734ef3d725fc7a99`  
		Last Modified: Mon, 09 Dec 2024 19:29:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3050ffc3c19773a71bc3b1026cfc174ec32b3a97b6dd42f8ac2d6d3a95d64ca3`  
		Size: 297.2 MB (297168489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:5e456cfb80f91f5d184b9a016c089e378e268ff233ecfd93373ccf9b99e7af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37550374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4db618f5c3f4aafdd64ac2bb53af5858f584fbaa8cc3bc52dd1f039e41eb0c`

```dockerfile
```

-	Layers:
	-	`sha256:f13305cf555b2104abb7d8a0782217856fcd51f2b18e354ea105c5e5c373f6dd`  
		Last Modified: Mon, 09 Dec 2024 20:39:35 GMT  
		Size: 37.5 MB (37541712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a781552e8708b7f1ff4f52aa3cefb93f05dc179ea71dc170313789b30fb98e9f`  
		Last Modified: Mon, 09 Dec 2024 20:39:31 GMT  
		Size: 8.7 KB (8662 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:4c294e47eb3752542b824618f8e95835909e27dfa14fa0b39f6410647d201da8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:3eea476332ca8c66ec98ca233191dd532eda7bea616f5a110fd8707f454b6df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609309801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0a27d0cf973beeeefbf7f38f32193c9cbbfe9e005372687d6a0fbf2e3cbaac`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
EXPOSE map[11345/tcp:{}]
# Mon, 09 Dec 2024 12:55:29 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Mon, 09 Dec 2024 12:55:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Mon, 09 Dec 2024 12:55:29 GMT
CMD ["gzserver"]
# Mon, 09 Dec 2024 12:55:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.15.1-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b27724939102ee35a9cdb48f34f5216667c81055955817b5cbbc269506bd1`  
		Size: 1.2 MB (1198847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fb44c058ddabcd4051befdffe65128238e5ec5036d38d25a65d857c1c0f28`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 5.4 MB (5361907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef3641eabd1611f862c208ee8576714e8a0a0253ccd0de885409f3f7e2e5676`  
		Last Modified: Mon, 09 Dec 2024 19:29:15 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5384edf40a924ba3b6e4ebea240776edf6ea3cff04a008b1c2ab82791b7dec37`  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e5c66f313291a95c156136e84c6a59e3ed3fd2443298d634c66303bf2a69e`  
		Last Modified: Mon, 09 Dec 2024 19:29:19 GMT  
		Size: 278.1 MB (278067567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d712a32f72d4975eb3825b3bed247e3f30513bd2d50f68734ef3d725fc7a99`  
		Last Modified: Mon, 09 Dec 2024 19:29:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3050ffc3c19773a71bc3b1026cfc174ec32b3a97b6dd42f8ac2d6d3a95d64ca3`  
		Size: 297.2 MB (297168489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:5e456cfb80f91f5d184b9a016c089e378e268ff233ecfd93373ccf9b99e7af68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37550374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4db618f5c3f4aafdd64ac2bb53af5858f584fbaa8cc3bc52dd1f039e41eb0c`

```dockerfile
```

-	Layers:
	-	`sha256:f13305cf555b2104abb7d8a0782217856fcd51f2b18e354ea105c5e5c373f6dd`  
		Last Modified: Mon, 09 Dec 2024 20:39:35 GMT  
		Size: 37.5 MB (37541712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a781552e8708b7f1ff4f52aa3cefb93f05dc179ea71dc170313789b30fb98e9f`  
		Last Modified: Mon, 09 Dec 2024 20:39:31 GMT  
		Size: 8.7 KB (8662 bytes)  
		MIME: application/vnd.in-toto+json
