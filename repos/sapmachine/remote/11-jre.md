## `sapmachine:11-jre`

```console
$ docker pull sapmachine@sha256:42fb4d9deca998197c40948000c84c5ce9b845002b74ec3e80099ca729f03091
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:94b917f799c51b10b559dc1e8d5203d31cfe06a9e2d460b35701c8b42e3ad84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79833517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971e1c84aa43841c443800a0f50ace8ba61cff04985a29284d31cad479087a00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:26:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979f4a558f1244a2129a086d6e6556c86e3fd2d06aac42e3c8b917175abda034`  
		Last Modified: Tue, 17 Mar 2026 02:26:19 GMT  
		Size: 50.1 MB (50101524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c6e5ed7fe7337fb7b46de7dd9dd65a6a33e67f0963569047a07f441fc5e006ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40ac725a5511c3086b745a954d798bb0cb8872103e2228566047aeb996603cc`

```dockerfile
```

-	Layers:
	-	`sha256:ceb64f9828c42b603e10562f0de2f34c77670045336134d2027de6f1ebae8b8d`  
		Last Modified: Tue, 17 Mar 2026 02:26:18 GMT  
		Size: 2.5 MB (2523685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2976c12660fde8a06d1f550a2b9ddeb1eb9f4c16fd2fffd49a49cacf15726920`  
		Last Modified: Tue, 17 Mar 2026 02:26:18 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json
