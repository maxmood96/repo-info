## `azul-zulu:21-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:05ed2239cc1615028c9e1bb34b1d7a76a1006d4174b5bc2568b79e87fb69e0e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6f9b666e471f1c0416f678d83d3e29e17e5ba0c418566e16e0cff3d6ae4cc86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233296301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c209acce7dc71e8d90e22b360d37c60256be36997f8edb0681f718c9bde2b262`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:15 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:15 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:19:15 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec425d9fbb2d8042daaddc76e3babd8abe1b3afc0d53fcaa0b1de5bcf53b8c1`  
		Last Modified: Wed, 27 May 2026 00:19:31 GMT  
		Size: 164.7 MB (164735988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c498e11b4406978271b7e71af802604062fecdc2f2422d6a9ee8615ff4581754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2544a7edfb860c83dd2db27f24f24cf6cb413a880f28d6fd2a261f28dd0cc0c1`

```dockerfile
```

-	Layers:
	-	`sha256:fe7a0bd8bc72042d70d8c31eecd922b6b6f1813ea9ec8002fdb394fd85aeadbd`  
		Last Modified: Wed, 27 May 2026 00:19:27 GMT  
		Size: 9.2 KB (9238 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:905e205d72bb324c2e4e379c9381e680d72c7e06fb2ff3e2512f72750d514005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa23b9a3f0e98c8c2cc8aeb01eb5026c9b83fdc8fd46fc8b7c4ae9fc03eb9956`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:43 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:43 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:18:43 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fef0b26d67a996d5ac401f67a3f9a23901a8daaae203f08cdf187ed3ec6b07`  
		Last Modified: Wed, 27 May 2026 00:19:01 GMT  
		Size: 164.0 MB (164038521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c528264b5d5f6bf8a210faab19a83ab11d202e7a1b26240d436dce6c3ed9d4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d24fe7748c49635af9942d14027a130e8a168fd9e0357ee899f021ea7a3fb4c`

```dockerfile
```

-	Layers:
	-	`sha256:f9c6416e3434618cc11299955c39b4373fc6f9461446c795ddf8cab99823f4f8`  
		Last Modified: Wed, 27 May 2026 00:18:57 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
