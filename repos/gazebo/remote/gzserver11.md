## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:4017847bd5406e1e255efc55a192c57dbdc7b4b8691e51abb1f4906d9fded61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:5297e7a0cf7d1686fc28a4150c8aba0ac4f9d8d5ac78d6bd0a2407f19709035c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313399073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519431adfc406f9fa95ae950f31e54581b1d90abe23792e88d74719587aa0263`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:10 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:36:10 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 05 Jun 2024 05:38:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:38:14 GMT
EXPOSE 11345
# Wed, 05 Jun 2024 05:38:14 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 05 Jun 2024 05:38:14 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 05 Jun 2024 05:38:14 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead13979c3370f825d55d7e6c1cfeff87719e71c87c099a7f9da0c57968a412d`  
		Last Modified: Wed, 05 Jun 2024 05:43:15 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1c4655e2401a0cc7ed5e343bca0e10b2a12f6cc3c0f0d96aa267270a1cb5b4`  
		Last Modified: Wed, 05 Jun 2024 05:43:15 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce72973bf96d3e4a9ca47e9d16c278c825b4621338e46a5e8343b5daa5c4f00`  
		Last Modified: Wed, 05 Jun 2024 05:43:46 GMT  
		Size: 278.1 MB (278060441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26207d28b425e64222f9c4821313fcf94eb4676274b217f269587a84e25edb0`  
		Last Modified: Wed, 05 Jun 2024 05:43:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
