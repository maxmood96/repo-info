## `azul-zulu:11-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:93c894cfdda83754ec43fee5cfff439fbe49cbe977afebb8c929852041f27166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:87568e4bbfe4e8912f2a80c31a67d6627aebef5df9ce469be29916ce37f1045a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215685930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd20b2b6bcc5f485004f26a01ec04737ca6488207e165a83b1894eab64cbef4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:36 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:36 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:36 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca463db68bed4e0cd4ff936aa4155fa9193c813536c7b9186e6c937d1819013`  
		Last Modified: Wed, 27 May 2026 00:18:54 GMT  
		Size: 147.1 MB (147125617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:47e582ba51ad99d162c9e5a19fffa17a4b8f9b6d7c467225d9fa22a70e615e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb03a50f4fb57c7f4d1d953334ff39deeb3883a4a0df9400a0e9ed1384e0f258`

```dockerfile
```

-	Layers:
	-	`sha256:fc1d1b151e246a041871a50c26722f6b0507fe047cb223340bb3959ff0630f2a`  
		Last Modified: Wed, 27 May 2026 00:18:48 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5bf40cdbf3a6ed9d0b9003b546cc6a3b79cb002d252dfe25e8efd3c5dc4b2308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213940612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3d22c9b747c3c0b04ace3aa2adebebc2ee5c550d8975a95465c5ed31be2577`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:11 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:11 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:11 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c644354c6798168a5c10b253c1cb3abfe3f91e0cac669af1f9ab21f2bccc37`  
		Last Modified: Wed, 27 May 2026 00:18:29 GMT  
		Size: 146.8 MB (146808878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4c313561545bfdec730eb12bdfecf228daf715591fe1611a332f1bbff8ba7484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440508d0656e74ba28885b0f54380666f859690457c3676687bb561c5c56d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:d0ba15175b7539e822ba62c628ea38e3cb7afdb429eb5744ba9878eae5c073e7`  
		Last Modified: Wed, 27 May 2026 00:18:24 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
