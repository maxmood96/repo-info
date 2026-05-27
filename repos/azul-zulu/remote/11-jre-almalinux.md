## `azul-zulu:11-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:362584ccdea9ca5dd121d9c6be9876535e05a5ca18172194c6ae84b49c18d9c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:413cd5cfc43c0d9a185770f323e45f8d613617cff15d2282a9935058abc46a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134926788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f828bb65c9b0903ca921860c6177e18976f41e5fbf37770ff73fca1bf39f9ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:34 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:34 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7257c965928ca5f3167dd1cc298a47549b96de49197591bd3ceda5bc0bb72d0`  
		Last Modified: Wed, 27 May 2026 00:18:45 GMT  
		Size: 66.4 MB (66366475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:50e5e11cf1826df16694c9ff5b64c76700617dbe4167f333ee5a9fc55f657bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9e54a39e9d14649758385d1210349dc126aae66058d88176f87f1333964ad8`

```dockerfile
```

-	Layers:
	-	`sha256:51855282da932dd57092b75221b78c3b15d2f44599cf4722c2fbd76f10d92321`  
		Last Modified: Wed, 27 May 2026 00:18:43 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:94bc99c3e2cbd92dff483258758cb668361a9a762f17cf07694e98719270b6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133317001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5288db8d674acd7c152d529b6e0aba40f19d68b7bed162910d18914914d74f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:08 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:08 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da8253a7c3b48825d204d80be7de8e052242acefa5dab1d903f36014a0df671`  
		Last Modified: Wed, 27 May 2026 00:18:20 GMT  
		Size: 66.2 MB (66185267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:24e52b9828ff0a11d2249d8b2c22d5fb68ebd42aa6c80b9d95f7dda640c7bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c6e6258ef3d20bba050c9aa591cc82c34140dad8cfa42b3241625644861ae`

```dockerfile
```

-	Layers:
	-	`sha256:5ff14794e5ddf59c5e076fcb29b799e319c20fe20d476def6a5ae51bc0278b60`  
		Last Modified: Wed, 27 May 2026 00:18:18 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
