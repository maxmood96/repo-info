## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:6fef46479de5fc055a1f16cbc6fc823c19619bb72e6723d6644d8da02016ce46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:aa637d5536602da80983d173232a8fb58c85b3a5676840ec22094d93b679b735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.2 MB (609239107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40778f17324307d1c4a4e4824e2d0bc246c056eaeb62f04936a5196ccd284aed`
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
	-	`sha256:8b2b5ac33b1af709f54bf1502bb34bc2f734a06ba2c1c3d839cded36358d9c51`  
		Last Modified: Fri, 05 Jul 2024 20:54:07 GMT  
		Size: 297.1 MB (297111307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gazebo:libgazebo11` - unknown; unknown

```console
$ docker pull gazebo@sha256:5d7b81f104789fbff207defa869ed06ca58dfe2502e58fdb92dbced51ed60d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37277961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2065c97e51722a5d652bcda2003ea582b3a14d3d606ad71ca0d9c961a3ba3f0c`

```dockerfile
```

-	Layers:
	-	`sha256:f5b7369aa1f44b2732682fc0f3431f4fc267d105c2e32be0af3408a918b5ca5b`  
		Last Modified: Fri, 05 Jul 2024 20:54:02 GMT  
		Size: 37.3 MB (37269331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9d0d468472e332c6c05ed459a911e94bf3ff82a45763b9969f78a46110acea`  
		Last Modified: Fri, 05 Jul 2024 20:54:00 GMT  
		Size: 8.6 KB (8630 bytes)  
		MIME: application/vnd.in-toto+json
