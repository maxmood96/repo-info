<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gazebo`

-	[`gazebo:gzserver11`](#gazebogzserver11)
-	[`gazebo:gzserver11-focal`](#gazebogzserver11-focal)
-	[`gazebo:latest`](#gazebolatest)
-	[`gazebo:libgazebo11`](#gazebolibgazebo11)
-	[`gazebo:libgazebo11-focal`](#gazebolibgazebo11-focal)

## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:fe478968aeb5013c2753b0349cb5e97efff08ee6aee5843dd01a83ef0add2a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:572c6be1d44e3c5c27b48e885f5c710dc01d5fd668fb66e2f04aff805a947521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312126575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268efd6351d5ed05290fb1c208fa05c7d32215a81510d796829837f3b010acd`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
EXPOSE map[11345/tcp:{}]
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e633987239294f68bc645f7dc9db24b616d70d1a5d0cc16cbf24d3165acbe`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 1.2 MB (1198837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cbfaea2d31922ae9cb1bdd84a0f680a24f2594db0a3ffe9a18cc4a0e840ad`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 5.4 MB (5361863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dff08a5a9954ee6e10f522bb3eb0f1ef576d5ffe525e4152232e8312af32f`  
		Last Modified: Wed, 16 Oct 2024 16:16:40 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433770b6b22a8774f20e08b9eb1310e6a9bff8605215b9425835e8652b7ff6fa`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c4cc642c2f6cdfd7894459f124589169dd4f1ecafa5ffad2495b45dc356f9f`  
		Last Modified: Wed, 16 Oct 2024 16:16:46 GMT  
		Size: 278.1 MB (278052887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b4c6ed6e0459748f0199cd8120978eb129ee26ccbe025ef8988500bcf7a86`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11` - unknown; unknown

```console
$ docker pull gazebo@sha256:91dcf63911bfd450fa334b549d4b934e05ee3521ed5d05659946144f55b9b609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6571212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65aa5c10673263951f483a37f712b18f818998b7686f48f6b4423e7d665d8`

```dockerfile
```

-	Layers:
	-	`sha256:05ca54fdfc928584e082ec85c220744086a83d724ad1076283ccabb605fad2f2`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 6.6 MB (6555073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fd53237917692d0e050c59856c2419bc0e81a1486a1736dda3195c7c2314c3`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 16.1 KB (16139 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:fe478968aeb5013c2753b0349cb5e97efff08ee6aee5843dd01a83ef0add2a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:572c6be1d44e3c5c27b48e885f5c710dc01d5fd668fb66e2f04aff805a947521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312126575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268efd6351d5ed05290fb1c208fa05c7d32215a81510d796829837f3b010acd`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
EXPOSE map[11345/tcp:{}]
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e633987239294f68bc645f7dc9db24b616d70d1a5d0cc16cbf24d3165acbe`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 1.2 MB (1198837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cbfaea2d31922ae9cb1bdd84a0f680a24f2594db0a3ffe9a18cc4a0e840ad`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 5.4 MB (5361863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dff08a5a9954ee6e10f522bb3eb0f1ef576d5ffe525e4152232e8312af32f`  
		Last Modified: Wed, 16 Oct 2024 16:16:40 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433770b6b22a8774f20e08b9eb1310e6a9bff8605215b9425835e8652b7ff6fa`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c4cc642c2f6cdfd7894459f124589169dd4f1ecafa5ffad2495b45dc356f9f`  
		Last Modified: Wed, 16 Oct 2024 16:16:46 GMT  
		Size: 278.1 MB (278052887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b4c6ed6e0459748f0199cd8120978eb129ee26ccbe025ef8988500bcf7a86`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:91dcf63911bfd450fa334b549d4b934e05ee3521ed5d05659946144f55b9b609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6571212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c65aa5c10673263951f483a37f712b18f818998b7686f48f6b4423e7d665d8`

```dockerfile
```

-	Layers:
	-	`sha256:05ca54fdfc928584e082ec85c220744086a83d724ad1076283ccabb605fad2f2`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 6.6 MB (6555073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65fd53237917692d0e050c59856c2419bc0e81a1486a1736dda3195c7c2314c3`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 16.1 KB (16139 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:latest`

```console
$ docker pull gazebo@sha256:0c3c8d6dcffcf06280541d9dd5dbc97e29f22e0cf488940cbdf0e227f3152c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:fee665665f4c00c246276ec324cf093126531777104bdfbdfa631c667637d02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.2 MB (609242743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce9d6c81e16b8e14c883e8de38a32ee0c432516c400843dd803efc142798be1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 10 Oct 2023 09:44:30 GMT
ARG RELEASE
# Tue, 10 Oct 2023 09:44:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Oct 2023 09:44:30 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["/bin/bash"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
EXPOSE map[11345/tcp:{}]
# Tue, 10 Oct 2023 09:44:30 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["gzserver"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e633987239294f68bc645f7dc9db24b616d70d1a5d0cc16cbf24d3165acbe`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 1.2 MB (1198837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cbfaea2d31922ae9cb1bdd84a0f680a24f2594db0a3ffe9a18cc4a0e840ad`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 5.4 MB (5361863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dff08a5a9954ee6e10f522bb3eb0f1ef576d5ffe525e4152232e8312af32f`  
		Last Modified: Wed, 16 Oct 2024 16:16:40 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433770b6b22a8774f20e08b9eb1310e6a9bff8605215b9425835e8652b7ff6fa`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c4cc642c2f6cdfd7894459f124589169dd4f1ecafa5ffad2495b45dc356f9f`  
		Last Modified: Wed, 16 Oct 2024 16:16:46 GMT  
		Size: 278.1 MB (278052887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b4c6ed6e0459748f0199cd8120978eb129ee26ccbe025ef8988500bcf7a86`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148ad3724853d3ec2465a7af854fb9d46051de349108fd8cf22f0c36dfce0a`  
		Last Modified: Wed, 16 Oct 2024 16:53:12 GMT  
		Size: 297.1 MB (297116168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:latest` - unknown; unknown

```console
$ docker pull gazebo@sha256:f14550c3864c123ef1a20ff0431707427c2bbc0407606d733a570789de1ddfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44eed3b8fee6e11b7fd77f01942084e6b3b29e061d689c910bf022cd49efa9a`

```dockerfile
```

-	Layers:
	-	`sha256:2a24fe47718fd06ef0a9034b17ca50ef25f7756d77066f68f10d406866ac35b6`  
		Last Modified: Wed, 16 Oct 2024 16:53:09 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dea80e27c44e4a75d6b54bda85ddebad8484a88f5d67b4cf269c0a1ef908104`  
		Last Modified: Wed, 16 Oct 2024 16:53:08 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:0c3c8d6dcffcf06280541d9dd5dbc97e29f22e0cf488940cbdf0e227f3152c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:fee665665f4c00c246276ec324cf093126531777104bdfbdfa631c667637d02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.2 MB (609242743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce9d6c81e16b8e14c883e8de38a32ee0c432516c400843dd803efc142798be1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 10 Oct 2023 09:44:30 GMT
ARG RELEASE
# Tue, 10 Oct 2023 09:44:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Oct 2023 09:44:30 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["/bin/bash"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
EXPOSE map[11345/tcp:{}]
# Tue, 10 Oct 2023 09:44:30 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["gzserver"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e633987239294f68bc645f7dc9db24b616d70d1a5d0cc16cbf24d3165acbe`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 1.2 MB (1198837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cbfaea2d31922ae9cb1bdd84a0f680a24f2594db0a3ffe9a18cc4a0e840ad`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 5.4 MB (5361863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dff08a5a9954ee6e10f522bb3eb0f1ef576d5ffe525e4152232e8312af32f`  
		Last Modified: Wed, 16 Oct 2024 16:16:40 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433770b6b22a8774f20e08b9eb1310e6a9bff8605215b9425835e8652b7ff6fa`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c4cc642c2f6cdfd7894459f124589169dd4f1ecafa5ffad2495b45dc356f9f`  
		Last Modified: Wed, 16 Oct 2024 16:16:46 GMT  
		Size: 278.1 MB (278052887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b4c6ed6e0459748f0199cd8120978eb129ee26ccbe025ef8988500bcf7a86`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148ad3724853d3ec2465a7af854fb9d46051de349108fd8cf22f0c36dfce0a`  
		Last Modified: Wed, 16 Oct 2024 16:53:12 GMT  
		Size: 297.1 MB (297116168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:f14550c3864c123ef1a20ff0431707427c2bbc0407606d733a570789de1ddfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44eed3b8fee6e11b7fd77f01942084e6b3b29e061d689c910bf022cd49efa9a`

```dockerfile
```

-	Layers:
	-	`sha256:2a24fe47718fd06ef0a9034b17ca50ef25f7756d77066f68f10d406866ac35b6`  
		Last Modified: Wed, 16 Oct 2024 16:53:09 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dea80e27c44e4a75d6b54bda85ddebad8484a88f5d67b4cf269c0a1ef908104`  
		Last Modified: Wed, 16 Oct 2024 16:53:08 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:0c3c8d6dcffcf06280541d9dd5dbc97e29f22e0cf488940cbdf0e227f3152c4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:fee665665f4c00c246276ec324cf093126531777104bdfbdfa631c667637d02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.2 MB (609242743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce9d6c81e16b8e14c883e8de38a32ee0c432516c400843dd803efc142798be1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 10 Oct 2023 09:44:30 GMT
ARG RELEASE
# Tue, 10 Oct 2023 09:44:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Oct 2023 09:44:30 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Oct 2023 09:44:30 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["/bin/bash"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
EXPOSE map[11345/tcp:{}]
# Tue, 10 Oct 2023 09:44:30 GMT
COPY ./gzserver_entrypoint.sh / # buildkit
# Tue, 10 Oct 2023 09:44:30 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 10 Oct 2023 09:44:30 GMT
CMD ["gzserver"]
# Tue, 10 Oct 2023 09:44:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e633987239294f68bc645f7dc9db24b616d70d1a5d0cc16cbf24d3165acbe`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 1.2 MB (1198837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819cbfaea2d31922ae9cb1bdd84a0f680a24f2594db0a3ffe9a18cc4a0e840ad`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 5.4 MB (5361863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3dff08a5a9954ee6e10f522bb3eb0f1ef576d5ffe525e4152232e8312af32f`  
		Last Modified: Wed, 16 Oct 2024 16:16:40 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433770b6b22a8774f20e08b9eb1310e6a9bff8605215b9425835e8652b7ff6fa`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c4cc642c2f6cdfd7894459f124589169dd4f1ecafa5ffad2495b45dc356f9f`  
		Last Modified: Wed, 16 Oct 2024 16:16:46 GMT  
		Size: 278.1 MB (278052887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b4c6ed6e0459748f0199cd8120978eb129ee26ccbe025ef8988500bcf7a86`  
		Last Modified: Wed, 16 Oct 2024 16:16:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9148ad3724853d3ec2465a7af854fb9d46051de349108fd8cf22f0c36dfce0a`  
		Last Modified: Wed, 16 Oct 2024 16:53:12 GMT  
		Size: 297.1 MB (297116168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:f14550c3864c123ef1a20ff0431707427c2bbc0407606d733a570789de1ddfbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44eed3b8fee6e11b7fd77f01942084e6b3b29e061d689c910bf022cd49efa9a`

```dockerfile
```

-	Layers:
	-	`sha256:2a24fe47718fd06ef0a9034b17ca50ef25f7756d77066f68f10d406866ac35b6`  
		Last Modified: Wed, 16 Oct 2024 16:53:09 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dea80e27c44e4a75d6b54bda85ddebad8484a88f5d67b4cf269c0a1ef908104`  
		Last Modified: Wed, 16 Oct 2024 16:53:08 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json
