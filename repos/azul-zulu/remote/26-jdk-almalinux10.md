## `azul-zulu:26-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:4b7dff60acb444dbae78be235b95a41e9e99c5f583eec1b1468dba3e0ff12215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:825fe54a1a71f46e32c0dd12f344ae7d79f831a05fff4e089465e5ba25906c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255310876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f940275621e2f0d84db5902ca6fbc2ec2dcb32f6250dc8465610f9bd4c1c6482`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:52 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:52 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:19:52 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4100698d31c0b6e06b3aa3d5f149715f3001558ea43e5a9c73af23ad5a27949`  
		Last Modified: Wed, 27 May 2026 00:20:12 GMT  
		Size: 186.8 MB (186750563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a5c458a53e2f4d40cff7fd5226a77a98d3b9df224b15b48cf0eb1efeb45d6654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ed13c780a3ea3c4e9cdb0d7300a30220210c5b87cec90f8b61948b0b8e4269`

```dockerfile
```

-	Layers:
	-	`sha256:8304e8b9eaff4220703333787dc8151aa271c9a2ec8fc0b9ebcbb5e9bce7923c`  
		Last Modified: Wed, 27 May 2026 00:20:07 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1e02a6372a5bd8cbc236731f6747718021d4f8f668a0a221ceee00a567ff5757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253583895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f2ce7406e4d991562fc8d1f12ba4570fc5bc4d7c91bbc3434a15eb37d53e0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:08 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 27 May 2026 00:19:08 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec68cf7f6d98fd0c6a01e6ee1b5e371708e66cb59220327b9043ed1d733678c8`  
		Last Modified: Wed, 27 May 2026 00:19:28 GMT  
		Size: 186.5 MB (186452161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a624835907765081970067edad02f4f844779737df9ed1fbde9607409a6d7ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d924eb03c01840dc31dd1c1979642b552cba276c6bef6db1e05a213ca6b998d`

```dockerfile
```

-	Layers:
	-	`sha256:4c24267f9909df2e195c309c16a1f236c0d38d895fb247820350ff2ccf11c459`  
		Last Modified: Wed, 27 May 2026 00:19:24 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.in-toto+json
