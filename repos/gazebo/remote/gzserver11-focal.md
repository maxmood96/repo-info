## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:2c58bd8bb77e355d011d2151224368049d701340df7dccba9e41475f76d6c377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:ea195dad0f82eae29efb98677eb29bb7c258d084cf366f6905c7ff29a24fbdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312127800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c27d238ecc2ed884da03f4aa3627a49896839e962ca1d33d967515a5a6a5a9`
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
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55947f7dbc106a39213d089d1418c502b8b2b89a136b327687d956ae544899f`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 1.2 MB (1198618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4733f1f65d23e29e11f9e66824e6d9b861251c11969c23cee0d6f2c9ddd3e`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 5.4 MB (5361668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d018a2d5f340ece470ef1ce68d21ef8df122e9adb144c3e3ab79cdb4e88566`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28b1413d020066523a95c7cfc0b0380234b9cb86ee4716304089fc35c4afbc`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e932e6f2f16c815362f0aec0480fa80f95f64b1ecc10ff8bded2675cf2a3871d`  
		Last Modified: Fri, 05 Jul 2024 19:57:40 GMT  
		Size: 278.1 MB (278053813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a45a1a688c608a7a8e1c4e366df657aa434cb39210a4abbd7e028bdac37884`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:gzserver11-focal` - unknown; unknown

```console
$ docker pull gazebo@sha256:a4c5c2440f53d6eea3945cdeec8e815d15a9b7a370f11a55d2247c295c0172b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f08705391bf15f85aba9fe7c94c1badbad02d054cb01341af53c9b941fdec3`

```dockerfile
```

-	Layers:
	-	`sha256:e45c5ea79217170d4dc432fe938452dfc1ab35a2cb1acabcd3d0e5be987fac01`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 6.5 MB (6455590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044c3aa481a3a8866615df822f2bf022a53d68df0d2441a6c4b2faaefd6c06e8`  
		Last Modified: Fri, 05 Jul 2024 19:57:36 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
