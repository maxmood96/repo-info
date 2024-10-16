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
$ docker pull gazebo@sha256:b5ba442af3ce030cbbbff2e45c1baa858cdd4625be245b69ac6d726a15ab6049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:f5d90f96b58a725ba4731082a57618a158c739333cff7f88400ad1114702cbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609253881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600fac0e71ae438f522b1d0535df1f3dbd26aa422c37c0c94ca50d3705bb1ff`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b954990adc3bfb29720946ed44148cbf79e3a41dee2aaebe297e8af1aef1269`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.2 MB (1198659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02ac265fab4845da67d107013a6248e2725979d4113be4ed0d4117da9ead442`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 5.4 MB (5361762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294690e8c0b6861ec87662e3fff051f415c79b82495d9d95a83bdc9d91c4de44`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e780a6c1c1b79b760201f16bbe98d7573ceff616e3a40b24ca3a9eda468e68`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24216c1793c49f424bf47128140dc46fb1b976850f508f4cc4065aed7b3f7eca`  
		Last Modified: Wed, 02 Oct 2024 01:59:38 GMT  
		Size: 278.1 MB (278053156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a310d7637ff0e363097e9284c13bb9effff7cc65ffb5b1e9a621c481993acc`  
		Last Modified: Wed, 02 Oct 2024 01:59:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed363ecc6a7c650d86c23d78b60ff932828bc96a9290f26d95d87e35a69c2952`  
		Last Modified: Wed, 02 Oct 2024 02:59:50 GMT  
		Size: 297.1 MB (297127320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:latest` - unknown; unknown

```console
$ docker pull gazebo@sha256:4cbdeabc0c76212527f4b6080ab40612227803d1859049eb7d6762bdfec7fd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247805eeb75c5247ffa967e217ae66ebd8d9cc98199add9a2219f604476fb780`

```dockerfile
```

-	Layers:
	-	`sha256:fbf8a2ea591c79beb6d99a9c6d2b19c949e64e7f0172b5c2717732c8378b3573`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84e98a114cadc07606e68ba72b70ed558b2235936ca6cd0e0780372bdbbbfb6b`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 8.6 KB (8635 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:b5ba442af3ce030cbbbff2e45c1baa858cdd4625be245b69ac6d726a15ab6049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:f5d90f96b58a725ba4731082a57618a158c739333cff7f88400ad1114702cbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609253881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600fac0e71ae438f522b1d0535df1f3dbd26aa422c37c0c94ca50d3705bb1ff`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b954990adc3bfb29720946ed44148cbf79e3a41dee2aaebe297e8af1aef1269`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.2 MB (1198659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02ac265fab4845da67d107013a6248e2725979d4113be4ed0d4117da9ead442`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 5.4 MB (5361762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294690e8c0b6861ec87662e3fff051f415c79b82495d9d95a83bdc9d91c4de44`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e780a6c1c1b79b760201f16bbe98d7573ceff616e3a40b24ca3a9eda468e68`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24216c1793c49f424bf47128140dc46fb1b976850f508f4cc4065aed7b3f7eca`  
		Last Modified: Wed, 02 Oct 2024 01:59:38 GMT  
		Size: 278.1 MB (278053156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a310d7637ff0e363097e9284c13bb9effff7cc65ffb5b1e9a621c481993acc`  
		Last Modified: Wed, 02 Oct 2024 01:59:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed363ecc6a7c650d86c23d78b60ff932828bc96a9290f26d95d87e35a69c2952`  
		Last Modified: Wed, 02 Oct 2024 02:59:50 GMT  
		Size: 297.1 MB (297127320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:4cbdeabc0c76212527f4b6080ab40612227803d1859049eb7d6762bdfec7fd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247805eeb75c5247ffa967e217ae66ebd8d9cc98199add9a2219f604476fb780`

```dockerfile
```

-	Layers:
	-	`sha256:fbf8a2ea591c79beb6d99a9c6d2b19c949e64e7f0172b5c2717732c8378b3573`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84e98a114cadc07606e68ba72b70ed558b2235936ca6cd0e0780372bdbbbfb6b`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 8.6 KB (8635 bytes)  
		MIME: application/vnd.in-toto+json

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:b5ba442af3ce030cbbbff2e45c1baa858cdd4625be245b69ac6d726a15ab6049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:f5d90f96b58a725ba4731082a57618a158c739333cff7f88400ad1114702cbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609253881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600fac0e71ae438f522b1d0535df1f3dbd26aa422c37c0c94ca50d3705bb1ff`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b954990adc3bfb29720946ed44148cbf79e3a41dee2aaebe297e8af1aef1269`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.2 MB (1198659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02ac265fab4845da67d107013a6248e2725979d4113be4ed0d4117da9ead442`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 5.4 MB (5361762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294690e8c0b6861ec87662e3fff051f415c79b82495d9d95a83bdc9d91c4de44`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e780a6c1c1b79b760201f16bbe98d7573ceff616e3a40b24ca3a9eda468e68`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24216c1793c49f424bf47128140dc46fb1b976850f508f4cc4065aed7b3f7eca`  
		Last Modified: Wed, 02 Oct 2024 01:59:38 GMT  
		Size: 278.1 MB (278053156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a310d7637ff0e363097e9284c13bb9effff7cc65ffb5b1e9a621c481993acc`  
		Last Modified: Wed, 02 Oct 2024 01:59:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed363ecc6a7c650d86c23d78b60ff932828bc96a9290f26d95d87e35a69c2952`  
		Last Modified: Wed, 02 Oct 2024 02:59:50 GMT  
		Size: 297.1 MB (297127320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:4cbdeabc0c76212527f4b6080ab40612227803d1859049eb7d6762bdfec7fd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37455568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247805eeb75c5247ffa967e217ae66ebd8d9cc98199add9a2219f604476fb780`

```dockerfile
```

-	Layers:
	-	`sha256:fbf8a2ea591c79beb6d99a9c6d2b19c949e64e7f0172b5c2717732c8378b3573`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 37.4 MB (37446933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84e98a114cadc07606e68ba72b70ed558b2235936ca6cd0e0780372bdbbbfb6b`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 8.6 KB (8635 bytes)  
		MIME: application/vnd.in-toto+json
