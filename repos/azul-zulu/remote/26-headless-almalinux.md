## `azul-zulu:26-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:8f47343c3bc73d2c2d400385475aad8e8694e033a904bb0c74e19e7c8bced11d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ac2e6f2e89424008852c5e81b6bb98382fb0a683ec73be0fad7fb939d12ca0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254710101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa4c31948001ae0047b2d7d6ca5cf54d8e4f381d904a2f202ce47b2270de23`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:33 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:33 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:08:33 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a01491d10697be7d42b1da43ece0df54837881404497283fd46c2599a8124`  
		Last Modified: Tue, 02 Jun 2026 19:08:52 GMT  
		Size: 186.1 MB (186147639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:35552df559867ff7353c9776d9a39779cb7fc0156f919ce223e34aa751d4d957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e39fa783c53bc01fe03bf348d429d1d56284a2290d80a8aced1157288243ee`

```dockerfile
```

-	Layers:
	-	`sha256:061fd686e60b739895f393687c07c819957c809047bb0a6013d06ede79639b5c`  
		Last Modified: Tue, 02 Jun 2026 19:08:47 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:07b35ffcb1f3f218fb03f692ddfb3b067fb679b23c4c1e8109151241a8fdd2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252993500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7253c9ab9b2e034f117734271bf4a54527ba0f8d8053ec3e282f0f68b48a8f37`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:09:02 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:09:02 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:09:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:09:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:09:02 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:09:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb6eb4fadd16ef0d8b27f58f8ada5cefef66b96ff8e4fd7958b962d6c607f99`  
		Last Modified: Tue, 02 Jun 2026 19:09:23 GMT  
		Size: 185.9 MB (185851539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4eee50cdfc0bc370d8925f1b06e438158fa838874faf679b2e50369d4201e4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac85f8759f45c0351525bdf0a0204ae58112125995df8641b336f1c973dbdc3`

```dockerfile
```

-	Layers:
	-	`sha256:da33bbfd930a2c0f653b7cfbd6349d1dfcf0b7956947f2bb46d42838f2abdfc6`  
		Last Modified: Tue, 02 Jun 2026 19:09:17 GMT  
		Size: 9.3 KB (9324 bytes)  
		MIME: application/vnd.in-toto+json
