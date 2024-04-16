## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:ef39cf8c407e6c423ebf0bbe9ea68a55675ae84b3ee8b03dfe31609e3d33228d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:bfa3deaa5c24af309cc99b2e09ac330470f6bc5bd9d05e4733b820f2425c0662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.5 MB (610502821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eacd46c6904e22cfcad97b1ead6599233e93e433d7042b796c16511aabb008c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:27 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:30:28 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 16 Apr 2024 04:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:33:25 GMT
EXPOSE 11345
# Tue, 16 Apr 2024 04:33:25 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 16 Apr 2024 04:33:25 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 16 Apr 2024 04:33:26 GMT
CMD ["gzserver"]
# Tue, 16 Apr 2024 04:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91fa230d04b15442f9fdc43a8fa3b4a03c9fe8f08ce286f1d4a7b32cb1f590`  
		Last Modified: Tue, 16 Apr 2024 04:38:07 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7ead5b242d8095779a6aea1bf55c6fc1a6e457b86912f1edf6a2828953f0c7`  
		Last Modified: Tue, 16 Apr 2024 04:38:07 GMT  
		Size: 290.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046ba4637f1ac376cac9b737e495d613efdc31f0a0a17317ad52c41d8ea3b5d8`  
		Last Modified: Tue, 16 Apr 2024 04:38:38 GMT  
		Size: 278.1 MB (278056562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed904ba23be2e341f80af609a3cfbe0518f94949a12bec7b6d01d9f02f7d65eb`  
		Last Modified: Tue, 16 Apr 2024 04:38:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d325b602480d38961210f4480b347ac55d8b9319f6b34f3710886025a0bc50ad`  
		Last Modified: Tue, 16 Apr 2024 04:39:33 GMT  
		Size: 297.1 MB (297107484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
