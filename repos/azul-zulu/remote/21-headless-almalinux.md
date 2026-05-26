## `azul-zulu:21-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:b1fa391f19cc2be8c4a7b2561225f3675aef391b6fc9f1d2218f29996577f272
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7a71d156aa817e4c29ec5a149f8f6f01dec808ca12c27d7b78955a0613cdfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233244905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a105603e1e833d51c811e92fe128073066379a66847270681dcdb415c19f3b0a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:26 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:26 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff10bb9c52240d748952b4214f482d17bc50ac49ec28f0e25aa4fc2d6cb9542`  
		Last Modified: Tue, 26 May 2026 19:18:44 GMT  
		Size: 164.8 MB (164788868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9d595590ebf6795ab303ee65f7b2fe4a9582c5ae1da2f8dc366d25b7607ef8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4e1d4b2fd8b0ca5ef4a4d44fd430cdb471b08fa79ed74c90446c461d9fa092`

```dockerfile
```

-	Layers:
	-	`sha256:0f10969be514121d4635c0c58a36f701f791ca67f41bcfe29083479d030ff2cc`  
		Last Modified: Tue, 26 May 2026 19:18:40 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a07bebd2d9fdf38725a66d89d0050577c964ab484f36ef0eab99e675a9b2a21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231061107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e9d510f25fdfd768fec75d2c79862133dcbbec3f0838736f778ea29238465d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:34 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:34 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 26 May 2026 19:18:34 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:18:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff456f59c33a99c3bd576ce0b7c2bab4352992fb88e2fac10886f3e6f936597`  
		Last Modified: Tue, 26 May 2026 19:18:52 GMT  
		Size: 164.1 MB (164090215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fc1b58468086e26e9e9c97b44efcd0abaaa7fb3aa436c6788b8f50ba3c74934d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93aac8b64abd176f74217294d4eac23b0cef4c7a548e8a70dca24a4b8fb1a4af`

```dockerfile
```

-	Layers:
	-	`sha256:4885b0aff81a1e3c1488762a5ae058928b09f56b83cf3902794b435571373563`  
		Last Modified: Tue, 26 May 2026 19:18:48 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
