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
