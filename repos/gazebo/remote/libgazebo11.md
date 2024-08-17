## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:bb8b9f106c84e20acb66fab6aad9a93fabf635a03e5720f2a0f125f203837225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:90e88d48b58f48ecd21af2c91740da8538a358b0779b108b37c18cb5fc80fe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.3 MB (609261103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cc554049aa37d1df59fdefa604295daaa8668370cdadf049c603c5fc6ee101`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:e000e2029f00214ccee82e47a3f51ec4d0fdfbcddaa5202427d649f33c1f6998`  
		Last Modified: Sat, 17 Aug 2024 04:08:47 GMT  
		Size: 297.1 MB (297136319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:99168aa043550009a70005d476246ef74406436d76bad8d0246e69d376c4ce18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37449659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7304ea9757173effd5c338e026b32ace3f747a8ed761669a02b79bcd9de3aa`

```dockerfile
```

-	Layers:
	-	`sha256:d46bc6f1ea7b7bf97ea2e43fd54cfe2d42b7d8ba2be33e981642640afd04ae1d`  
		Last Modified: Sat, 17 Aug 2024 04:08:40 GMT  
		Size: 37.4 MB (37441030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da278539a97f1a138b6374d3e48b4be7ef056e7014f01886d9bda0bdd8d25fb9`  
		Last Modified: Sat, 17 Aug 2024 04:08:39 GMT  
		Size: 8.6 KB (8629 bytes)  
		MIME: application/vnd.in-toto+json
