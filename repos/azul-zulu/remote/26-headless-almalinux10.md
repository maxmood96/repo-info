## `azul-zulu:26-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:bd80e07ba1611d2bd242744a216179e949656f0f45c4474146d183a611b5c4b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:81e3fd6f2929a52f7004f714eb0224dba7db6638c02ddab1ee45fbe0fd9199de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254654523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce87c7b47207002beb2758ef36a5099d6149aa7c06073a7f3ddf02d19b6e74f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:54 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:54 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:18:54 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4422dda729efcf92cfc04565428b2e8cb6d5daa9155a1d753985eb6838388729`  
		Last Modified: Tue, 26 May 2026 19:19:12 GMT  
		Size: 186.2 MB (186198486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:50cece92d6e2327f95d8dbf1f801ec27ecf98ec7213a38e61a9102210dea716b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21918096f2209be6fd8fedb3105b24c1fc43285e865964acd1b56378c848596`

```dockerfile
```

-	Layers:
	-	`sha256:cacb526a96096fc2db61db094c0af8bcf88ce9f8172776976598380fa5c851ea`  
		Last Modified: Tue, 26 May 2026 19:19:08 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2d861b8cf5fd7c50c23a51f944bea0dc93e79c8af88928db658d9c5c86075e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252872564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfd6e67193ca6dd8b258d61a40c3dfc8bee527b54d7b1a3027f52ee8ea1bb72`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:19:07 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:19:07 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:19:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:19:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 26 May 2026 19:19:07 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:19:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d2d54a3941d958130362a8c0c6c516a12abbe6bf991862ad514aa157397356`  
		Last Modified: Tue, 26 May 2026 19:19:27 GMT  
		Size: 185.9 MB (185901672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b179a66dca621561d9428332076387d8b351f06bda9fdc8bbdbc1d441bc2aa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af11fe4a4429b5cdae7e8d7be8ad0e189259e096006b477e16a1a5590b05dac`

```dockerfile
```

-	Layers:
	-	`sha256:21161347f0f5ad42e61ff21dd03b3fc21dd62e3c8197a51c53c3100bac85eef5`  
		Last Modified: Tue, 26 May 2026 19:19:22 GMT  
		Size: 9.3 KB (9324 bytes)  
		MIME: application/vnd.in-toto+json
