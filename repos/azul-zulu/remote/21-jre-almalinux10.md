## `azul-zulu:21-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:dd4a8c081c0eb589248ececb8a183cd13d8954958d9e822a6cbeb2666c52da8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ba54d9fc172317e0d559d48fd7b6c01a300e8a7a70f47a7bc02e75b5a1bbc9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144711085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a8fb111a8efb04a17bee61415a0e2218eb7ae1dfd9143ad0e5e0157cb0a237`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:16 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:16 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:19:16 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df002f1304a73f7fc6f784a59d0a0c19853b5f78df2bc0fec349a6841d4224c2`  
		Last Modified: Wed, 27 May 2026 00:19:29 GMT  
		Size: 76.2 MB (76150772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ebae265e8bf80be05722f7038994925d169e07af3cdce53c374920a48efd3979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ecf4c509aacbe71995f99088edd31cf2ae1dcb205ea608f14782bf3fdc94d1`

```dockerfile
```

-	Layers:
	-	`sha256:8dbdc9b5ebbfddae515bc47c528a769c39eb98f96f1264667e544d7163e87df8`  
		Last Modified: Wed, 27 May 2026 00:19:26 GMT  
		Size: 9.1 KB (9139 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:dfee8682bc0112e902ed72d09a37371735110457cd64bc7b8dd018fc181e0f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142940425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65d2e084d6454097a571a567f79c77cc5588eaa2bdc298f76aa840616b186af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:41 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:41 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:18:41 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097b930efd87e553be69998a7b6e91764c2b1a8bc8a0c309a1f63a4457a7c384`  
		Last Modified: Wed, 27 May 2026 00:18:54 GMT  
		Size: 75.8 MB (75808691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c94a3d82d159ecd811f04165bfa6f06f5a90064b57eff649710952e1460ed22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12327e0dbee7f3d66ef8431932eb87cfdf3a7536f187a3db1c17fe2c31bdec07`

```dockerfile
```

-	Layers:
	-	`sha256:0f4ae3ce537e71490850c03e1d365395b6f749739bd0e51d70f100c35a63ec2f`  
		Last Modified: Wed, 27 May 2026 00:18:51 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
