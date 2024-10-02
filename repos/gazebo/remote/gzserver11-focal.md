## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:ca9e86b8530594c4257625a8f374ac0f1531428d682024a8f3cee01008a35dcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:914c2dde13cea78401c83511089341722c063b7cac9006391244425fb4df46e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312126561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725f1b7b3d8b39c333bb53a3c12e7a3728f81049d8d82434fcba4aa9d012e5ae`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:6ee1d3e0829376a0c108cbb43bd63762ba586fd219cace70291001a50566c590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6571179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83118c421250e08af436a02b90a10a81d3b1dd46c40f58b4be445a1090d12c9d`

```dockerfile
```

-	Layers:
	-	`sha256:7bbec92856d0400e9ee6d9a55ff8f681aae94ec81b43fbae507512fa8b136f79`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 6.6 MB (6555073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac5d7dc1c4c48834f1d47b3e0cc9c473955e238bc1a1f2556310ca986d7b883`  
		Last Modified: Wed, 02 Oct 2024 01:59:30 GMT  
		Size: 16.1 KB (16106 bytes)  
		MIME: application/vnd.in-toto+json
