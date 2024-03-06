## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:63b67e27da8d51a95ae87c5952d96e3ada816a50954f5dc0dbad845802a0c1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:c51d16a4fb3906344410f709a31b445be0076406b8c61f4483ca5b1e8d19dc7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313220981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b205c3cc0c15863e3cb53cfc728221cf575c7bea6497299a0c61d0e7fafc54`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:02 GMT
RUN set -eux; 	key='D2486D2DD83DB69272AFE98867170598AF249743'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /usr/share/keyrings; 	gpg --batch --export "$key" > /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:19:02 GMT
RUN . /etc/os-release     && echo "deb [ signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg ] http://packages.osrfoundation.org/gazebo/$ID-stable $VERSION_CODENAME main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 06 Mar 2024 04:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.14.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:01 GMT
EXPOSE 11345
# Wed, 06 Mar 2024 04:22:01 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 06 Mar 2024 04:22:02 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 06 Mar 2024 04:22:02 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261375588b7961ac194ebb599469ed0e59bcb05e0621dc8e903fe9ccf721e4ba`  
		Last Modified: Wed, 06 Mar 2024 04:27:07 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac128ceeb4b0338e80f7e5691d6838c64a4db0c212bc4e888a1dd92c5cbd27a`  
		Last Modified: Wed, 06 Mar 2024 04:27:07 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993d348ded91d72d8e92f7864289a48a1d5ad0e877091fbeb4fd6d1ba5440434`  
		Last Modified: Wed, 06 Mar 2024 04:27:39 GMT  
		Size: 277.9 MB (277882479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50c014767d0115c169c1bf6257de9696fc8399f7be4ffdca6a97169c67b2df5`  
		Last Modified: Wed, 06 Mar 2024 04:27:07 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
