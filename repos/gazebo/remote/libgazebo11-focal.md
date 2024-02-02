## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:5c86183e42430c9c65cadfa643d75e636f914fa923e5a6440747d1491ca8da32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:f2fe1dd051855a5635635e97bfd8bc4342bbf96803887aa9d816c0732dc020d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.3 MB (610296295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088fef5565c88ef47a40bf41d61a31f61a98b46db03db164cc36d06d9a6e8bd2`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:41:46 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 06:41:47 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list
# Fri, 02 Feb 2024 06:45:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:45:35 GMT
EXPOSE 11345
# Fri, 02 Feb 2024 06:45:35 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Fri, 02 Feb 2024 06:45:35 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Fri, 02 Feb 2024 06:45:36 GMT
CMD ["gzserver"]
# Fri, 02 Feb 2024 06:53:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cd25045186d33d36e38fd71c8349c0206910a3d20c9334396c523687faa6f0`  
		Last Modified: Fri, 02 Feb 2024 06:53:40 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcef8ed793def9d8a1bde2332b01ff5a400bc566d5bea20e1ecb4e9659a26d8d`  
		Last Modified: Fri, 02 Feb 2024 06:53:40 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7784321839abe199136ad80f14f3e85e82b3f360f3b4e7c37583aafaf04877`  
		Last Modified: Fri, 02 Feb 2024 06:54:11 GMT  
		Size: 277.9 MB (277873202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650858cd76354ca239f83f3d8ad118344f72ce76a8fec478d486f09f9b42878b`  
		Last Modified: Fri, 02 Feb 2024 06:53:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898bc855ad4795eba4946b3c5bcd36ffa3b827b680a636476b8800c731652489`  
		Last Modified: Fri, 02 Feb 2024 06:55:07 GMT  
		Size: 297.1 MB (297080930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
