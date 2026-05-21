## `azul-zulu:11-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:cd3c7e4b98e931b3db5d330253f7f583e452d63483b3b5cc86fe520d9603ac73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6f5ea50a9801b69ea5f2e1aa52091419be725932823c80b183560f76bfbc17c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134447774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2b62b4dea78b61222cbf2373c0385744c6b26c34248c31ac519d4e15450c41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:26 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:15:26 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b907e24d092f12943f363964b8643fb0595ff892915cc42cf7a2a32564f44798`  
		Last Modified: Wed, 20 May 2026 21:15:38 GMT  
		Size: 66.0 MB (65991172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d86bf3561fd807f26f5ddaf79560b96aefbfd06383f681b1a88dcc44cf7abbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43754de601ee0d2450f75103512ce89a1d7159aba4833b7cb23904e78e7521`

```dockerfile
```

-	Layers:
	-	`sha256:f4d034bd8a3f1ec6ff77ab0b2a5c8d5fe5234688fe7c8af049e86dfcfb54efc0`  
		Last Modified: Wed, 20 May 2026 21:15:36 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c24a7a963005ae537df065f0e43dffa4bc5d149dec57a3020793f3a769e30b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132791041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace30bd299d1554b1414d60e8bad33978aeebb65cbdd446b0ee39f1c5f784324`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:27:49 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:27:49 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:27:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:27:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 20 May 2026 21:27:49 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fc820a9e91497fdeb9c7519926cfdbfb38a8fb0987ccfbae6464f3d6f6e1e1`  
		Last Modified: Wed, 20 May 2026 21:28:01 GMT  
		Size: 65.8 MB (65820872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:67f0694083855eaefbae1b9b0a0d0368caa11b7960d7cf66a0a8f006140af9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48414c85479a8fffb413aed07e1d0481445dbeb1eb0759367864f3410a3fdc6`

```dockerfile
```

-	Layers:
	-	`sha256:56f046c5697e8b4764d57488712e8697c3ff5fee2da201c8d9302e6a3513df38`  
		Last Modified: Wed, 20 May 2026 21:27:59 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json
