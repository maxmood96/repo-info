## `azul-zulu:26-jre-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:27629382edff8b189fc6c1b417042c28d8807d5afc1c678aa16fddfb5b93e4fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1e120e5c9a28660c9f01f52908d03509c8d7bd794331585673a5c1e08b5e84cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159582340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033ca1d207bd54b1b089d103e71e584a612bdff89d60284674cd1fa0dcd01be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:20:10 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:20:10 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:20:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:20:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:20:10 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d403f4da95216f7e2be045694e60f4a259f72dbe9bfc75c2863b231af339fd2`  
		Last Modified: Wed, 27 May 2026 00:20:25 GMT  
		Size: 91.0 MB (91022027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:552d642d86d51c6fb26f9dbb02ebe864f7208b80dd8919c0f89f92bfc3765679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55226ef38be5e97154ec925a876fc906a3be5343806b1698f0ec28048e8085fc`

```dockerfile
```

-	Layers:
	-	`sha256:307dd73fa44942b33c51a40917e2e0fec8cafb634837ce5b5b9e1d8fa4314073`  
		Last Modified: Wed, 27 May 2026 00:20:22 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3ebbb63fcfb5086c883b1380ab19e29bfadc5ef0c0aef0f90d86a9aa80184a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158075155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed0585b48d1483c91158ede1e505a662e9c12802649699237df7f9fb3227be2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:15 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:15 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:19:15 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc231d6940ad0ce2df29a8c46969a729cceccdd732b8f3335e81b5b031a5102f`  
		Last Modified: Wed, 27 May 2026 00:19:30 GMT  
		Size: 90.9 MB (90943421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d1999306077c238888064312007424a3f6961c3243bce137e89fcbb901bbdce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000ff203e71e45488160df9e88a765a49a317e7b2148398fada729ddc31b0033`

```dockerfile
```

-	Layers:
	-	`sha256:8623e5babf9bcdcd66d78e758975fc668490c85afefd346198464685ac4f72a1`  
		Last Modified: Wed, 27 May 2026 00:19:28 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
