## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:929f34d60a418881dd3ddc8446abc39d2e3ff424fc9cb414997a2429ab36d2c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:7c5172e0705c8ad6e7d7d803917779b8033f268b190bc5268c9af3afb0e651f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312124784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf4e523466e9e88e91b6539843393335a0bf9bbbc488a4c7f61b5f4ffbe30f8`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b4438bb56b00a7861b3f6c399ad8a0710bd1b267679a3e5c80b1d6c4ec903b`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 1.2 MB (1198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd82f4c6df1cef54bb94623483a983a58273ee9e6121170580969e9424ebf73`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 5.4 MB (5361680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cb438347637d05c15082eeee7bbbfe33d8511781e0f64f86f2c9e71162f6d0`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c9cdbb3bf7cfa04dcca73fa581a947c39e4e5e290cbb9b00e0d6ca5dd5656d`  
		Last Modified: Sat, 17 Aug 2024 02:01:09 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b1d4a40b600817b4ec0478e7245f0ddc7e147f1ef1a63f682f43514e1c384f`  
		Last Modified: Sat, 17 Aug 2024 02:01:13 GMT  
		Size: 278.1 MB (278050815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d55f7e67a94d64e8dd0e77292716eeed6e7246e98244e3bb6f72d758a8dc01a`  
		Last Modified: Sat, 17 Aug 2024 02:01:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:f59605fddf2cc2b8fd4281982bd32817691c0df91e7ba0c527fbb4bd60f1144d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6571161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0429690c9891c459f2e58df3917779864134225c18829d6870738e3841f476`

```dockerfile
```

-	Layers:
	-	`sha256:262b389c39da59a5f1cd70f31ae9944d6b7c7626ccf8ad256aa271ebed1d9211`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 6.6 MB (6555060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3069139711a08d2020b6ad8559a571edf45b01c2e2bce14df740144b4066304`  
		Last Modified: Sat, 17 Aug 2024 02:01:08 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
