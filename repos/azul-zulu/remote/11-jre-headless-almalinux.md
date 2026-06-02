## `azul-zulu:11-jre-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:86e2551f16424a4e0ec0af050f563d65a8bd574cc0fbb8412d815e8800ffe864
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:dd21fae1cfd050f5dc518e4c5ba0307e7e859b36db627a2e91777ef238e9c248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134510260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb45567cde22c43c1963a9a96250dcb63bab96e5e4fcc3bbec575c19ebf10c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:45 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:45 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:07:45 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10b3c9c9b44a5264c21870d1aaf1f2ce00caada15ea780a8938ea9107da5d39`  
		Last Modified: Tue, 02 Jun 2026 19:07:55 GMT  
		Size: 65.9 MB (65947798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7b4d95493235be3bb35c35102e13eae20eefeec475ae9121a8009e26728799e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf58e7cf7fb2e2c93a247b2e86d6df904cbe28cc4c4a419b0bf2b96c9581269`

```dockerfile
```

-	Layers:
	-	`sha256:4b5d069552d549297fe00c1ee18fe635c856b431277e93d21c09b38b23708e33`  
		Last Modified: Tue, 02 Jun 2026 19:07:54 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1e2a4ef5bb49fad9137277513e37721aa82d4fe6bca2714c27a1435aa5f22c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132917188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc88ec4bbe75a35d141f129e70e3b0cc1499926c8a1dcbe6be4249d74aa4761`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:03 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:03 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:08:03 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a1d5a3f2f35984f39f23b9dc40100f1c6341f3a50573e439ef9740d2615f7`  
		Last Modified: Tue, 02 Jun 2026 19:08:14 GMT  
		Size: 65.8 MB (65775227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:176ae46129e1e2604f0d8e30e3a8a570f9e32196949783bba5bf29bc6fdeac3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7825f877c123602ff69868f54d78c8f28637b3b687046ec019e7f17059df61`

```dockerfile
```

-	Layers:
	-	`sha256:eaa1116762f5baf16bf80d2b58f4b2e9c42eab094df3d5fb48cd16a232337cb6`  
		Last Modified: Tue, 02 Jun 2026 19:08:12 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json
