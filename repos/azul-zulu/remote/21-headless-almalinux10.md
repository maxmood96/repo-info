## `azul-zulu:21-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:43abec9ea235e031254ae1678128fd9b7fe4d309c5b8df9469f96e01e142aa03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9bc3c4c1537ab100653575a29315a54551ea423930803aa865f3e624840a2fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233301225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e85541d0a31a41731e80112a7bb1781d51ecca0dab91c2dea7efa5cf68074`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:12 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:12 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:12 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4217f4321dd218ee2447f463d0db10c46bb18a0c0cee59e9b2e70c54f2148dc4`  
		Last Modified: Tue, 02 Jun 2026 19:08:30 GMT  
		Size: 164.7 MB (164738763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:32ecdd891908fb11ea72936a11481a24c5370651ebb1a80827581d9195e14400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d819402a337862eb02ede3794200af0fab1cac5b36b8202f54911c0714648820`

```dockerfile
```

-	Layers:
	-	`sha256:823e1bb5054f52024051c703339bb1dda6166e480593a7a34622f72df7c1269a`  
		Last Modified: Tue, 02 Jun 2026 19:08:25 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f117f2f3dc1db6e197e172b76f03e822a644da5154fe3ca67e0573173ba736d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231184027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d08b460001622f20889f52c1f36d4405ef2881adeb77da4a8348f26f268bf7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:34 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:34 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec623ee6a399d3060406a515405dc94b340a8c7111be86fbac3b1161c4aed958`  
		Last Modified: Tue, 02 Jun 2026 19:08:52 GMT  
		Size: 164.0 MB (164042066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e7b74ab663223ac8014e6082fff85c2a02194b615af623c8ac940a418ee12fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d21ceb4ac00288f0788b243d02589c4b268e5646de32ae4ac2b79518daae1e`

```dockerfile
```

-	Layers:
	-	`sha256:6e24b31e0bd9c0894c201f50cfe597f4b2393f2356e8e875fbf1d3bbdbf54c64`  
		Last Modified: Tue, 02 Jun 2026 19:08:48 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
