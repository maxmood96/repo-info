## `azul-zulu:8-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:5dbe9828c5c9a99feb358caa169a12079f1f5006da823d175f1496b98b36dced
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6d9367691c3e981c19e2a11fca0bd7e67590e93d6234261ae57f8cadc7ecf722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128625513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f225c3f5c5d6bd888470bf6f3b8ecff44483a118b629ef649214f0551dbd3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:26 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:26 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 27 May 2026 00:18:26 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fdedfd23f500b5e88a26ef233de0d616ffa05dc4dbb4f713485ed199a50978`  
		Last Modified: Wed, 27 May 2026 00:18:36 GMT  
		Size: 60.1 MB (60065200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0f8f33cb9abbf78f553e95aeebf3efd6907b27af05b784942f59ce43518b487d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edc339f4fac925019bc7adf8bfb9dc4db278c2405dc0f89adea1e703eebf87a`

```dockerfile
```

-	Layers:
	-	`sha256:6274fe3b490b2a1662943038450b500a5e4d699d1447b96b137c75da02121c44`  
		Last Modified: Wed, 27 May 2026 00:18:34 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:52d9656624a9cc6c01a9cebf610d8a6f67d4e937fd88e30dd452e421642ea430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137154489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b7ec598e042f5d25f81ba73f94e6145877109e04c6526e5310258420676ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:01 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:01 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 27 May 2026 00:18:01 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15e34b996e12f0b1ca282abc558931b961a791dfce8c8e2fb3a711df7a2672f`  
		Last Modified: Wed, 27 May 2026 00:18:10 GMT  
		Size: 70.0 MB (70022755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:11ff306eec92bdf35acb0e4c93dc9cbd0f79c333df9303367d67556ecf4c5218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a33af3141cbd73f42d4e7f9d2b9cbd18b0c8e9602ff9f68b0cd1ffa4ead05c`

```dockerfile
```

-	Layers:
	-	`sha256:322daa1bcd55f335cb4d9820f8802379af7c22c3a4a62eac0dbfcb2930327280`  
		Last Modified: Wed, 27 May 2026 00:18:08 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json
