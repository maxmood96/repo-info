## `amazoncorretto:20-al2023-generic`

```console
$ docker pull amazoncorretto@sha256:2b81621f9fc0a6e19571031ed082d65fccc0b47c55015f368b179f4904c632df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2023-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b7c43ce494414249be4f2cc717656fcad197f48eba3c9e342c26ace904b45cef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260452124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa22d82d93b9114811729e09fc4af427d307c30e16ee9a6cebf39ce988a506f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:04 GMT
COPY dir:5aeab1edfeaa7561058aadd3dc752f2959c8cd0e5442b979406e3948fdedb852 in / 
# Tue, 29 Aug 2023 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:50:11 GMT
ARG version=20.0.2.9-1
# Tue, 29 Aug 2023 19:50:39 GMT
# ARGS: version=20.0.2.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Tue, 29 Aug 2023 19:50:40 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 19:50:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:8c169abda7fcf89d4baeaacf8e5d709a6112b4a6babe0c195a42404bca597f55`  
		Last Modified: Sat, 26 Aug 2023 03:05:59 GMT  
		Size: 52.3 MB (52287844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3bddaa1d9f800cd8b6a938df8065d82e5cf93049a3fa8423b8901327817ea`  
		Last Modified: Tue, 29 Aug 2023 19:59:42 GMT  
		Size: 208.2 MB (208164280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2023-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c84f6ab0349ff930ef6729328a9132bb9e7956c42b6c7f6edf4c0d28b10f42b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257444338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe67ce18cef280ab825de1b26eeac93cfe7319be9fd645d09f8c945509e5f11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:40:45 GMT
COPY dir:0004a2667b3e5dc5080ba46954457d05835caf07f7030d94b953f1c3cede9b0c in / 
# Tue, 29 Aug 2023 18:40:47 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:49:23 GMT
ARG version=20.0.2.10-1
# Fri, 08 Sep 2023 21:49:47 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && dnf install gnupg2 -y --allowerasing     && dnf install findutils -y     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && dnf install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && dnf remove -y findutils     && dnf install -y fontconfig freetype libjpeg dejavu-sans-fonts dejavu-serif-fonts dejavu-sans-mono-fonts libjpeg     && dnf clean all
# Fri, 08 Sep 2023 21:49:50 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:49:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:8e2acd49419010bc77a61e38a85963f09e403f004635f24c436d177a08df1040`  
		Last Modified: Sat, 26 Aug 2023 03:06:10 GMT  
		Size: 51.3 MB (51324150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519715d08dc2b6582a23a1ccc00d08a45d0430fe1d04afc01b5802072861fef`  
		Last Modified: Fri, 08 Sep 2023 22:00:07 GMT  
		Size: 206.1 MB (206120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
