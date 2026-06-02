## `azul-zulu:25-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:1c43b40b8190bfe3387e1e9b305be9e125d28ddf8840e2fcb1cb604f89de4493
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:30faccfeeeeb47a5da3771e88e093f4a7ef8607f977d25ad93f17188c86a6df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158862314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7770469495e00cd39ba919785d35120e3e38e5db16b3ce03eb53816e05f13bb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:27 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:27 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:27 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:27 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deadd0f7dd63d02ceecfddc60fcc016d0ff627590a9d1e954195cf4880cf5a72`  
		Last Modified: Tue, 02 Jun 2026 19:08:41 GMT  
		Size: 90.3 MB (90299852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:01a355e24d8347372cee77a60c74360a59042f10331bfa7c12b336d1cd232402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f6c05f68dbd9f0eb4dc4e8d197f3a55ce2c73281d5ecdbe986d316ceddaec9`

```dockerfile
```

-	Layers:
	-	`sha256:4001471670424db11e18516f001df7501a3981798a6f3a4146323f82543d29db`  
		Last Modified: Tue, 02 Jun 2026 19:08:38 GMT  
		Size: 9.1 KB (9138 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:77673a39d350fae4df9f7235b5a763eb688f4914f3d1d1a29144bccbf74e9952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157051499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3799b32d8dd5d622bf8e4a8b803eccd4a0ba697aab3c5ff49359cb502cacd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:46 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:46 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:46 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4b32615aad0acc4908e421e9249628882d964079c207194c5c66cae34173c1`  
		Last Modified: Tue, 02 Jun 2026 19:09:00 GMT  
		Size: 89.9 MB (89909538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f649b21d10588c6a891abf2d7f7ef5cb327e41396858f11b091e231f12b39669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d714f9c497448c223d46fae73240b1f2e1e9a0a87beed737b573209bb2489f`

```dockerfile
```

-	Layers:
	-	`sha256:798de9de0ef999ec2996fcb65e4af9bb74e80949aeeb6947fa1cf83d1dc659df`  
		Last Modified: Tue, 02 Jun 2026 19:08:58 GMT  
		Size: 9.2 KB (9230 bytes)  
		MIME: application/vnd.in-toto+json
