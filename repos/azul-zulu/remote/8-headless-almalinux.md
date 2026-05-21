## `azul-zulu:8-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:65d83ded36e85bef01c06dc3206af89f9e15216060725290baf84e61db9500e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:79eef280a7d5e75e20bc14045b4a20ca40f15e059cf91cfb9dc09029a45070df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128569468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc0b3b233eeb8aacd9d0e5a25fc8eb75718eda48f337cf9497767662eb6b1f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:14:48 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:14:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:14:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 20 May 2026 21:14:48 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1896df019edfe2b5b1dc45cd05e1909625db486b04fc2c892084f98cfd41f9`  
		Last Modified: Wed, 20 May 2026 21:14:58 GMT  
		Size: 60.1 MB (60112866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:27c3f182f6c89a653cff3e4d72d20a85f4ce8c4850f2a9fe9bbc646c665d5869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5735394aafbb56da932859d1f298f4463ecb3c716056d2ac27b56ab87a553f2`

```dockerfile
```

-	Layers:
	-	`sha256:82e364eeb06aa9e7170dd54f8c19f88e495da31a52cd3fd744a13ea9b7a93cd2`  
		Last Modified: Wed, 20 May 2026 21:14:56 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:66f9ed6ef67d1cc1c7bb01c77f0da99375a0f1ca87e5004c398fe29366ac0359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137043148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16191bb33a1af61c97e35cfb8a7a9cdbf9c3fe4466e7fb8d3191a7bcaa6595f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:27:04 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:27:04 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:27:04 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:27:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 20 May 2026 21:27:04 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19f512ae4483ce33e47b2f8579e75696d4fc0b1402bf0f8ca189657e2d6ad80`  
		Last Modified: Wed, 20 May 2026 21:27:13 GMT  
		Size: 70.1 MB (70072979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:105142b66f60acb67b9ed36f2c0c11537942ec10b91de5775a86f5f303d41156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119f0705c87ed5159882eb9ae65c2d91bddf9283d946ba899baa382a6f4e9c6c`

```dockerfile
```

-	Layers:
	-	`sha256:92af7b7a661db6750353a421c3de1d2d50e5c3f4d7714a897c71dd7e582af91b`  
		Last Modified: Wed, 20 May 2026 21:27:11 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json
