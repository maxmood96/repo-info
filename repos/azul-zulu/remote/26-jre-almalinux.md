## `azul-zulu:26-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:93ebd0e2f51757727775049d05faf3b492996127eb0777174116e19ffce7a7cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d2b48cdbb8176d34556331310b358d76920f92020edbb82689486673a0517fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159888975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218170fd461398914522439034f56e65ffde2b8437ee9d47944bba15297d1914`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:16:07 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:16:07 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:16:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:16:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:16:07 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662fce7ecd45bba9d6d8326384e7738778275f2276a0f540c76982dd8865e377`  
		Last Modified: Wed, 20 May 2026 21:16:22 GMT  
		Size: 91.4 MB (91432373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7616a8aafbc2da950c78daa1339b78577c63e155c3165a9b989b7a290b6ed69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a8e2ccf951283525274133f3cba058cfcb75b08df3ce20fc18bd8ab0b1fc1c`

```dockerfile
```

-	Layers:
	-	`sha256:10e8f013b0607404384676a9be95e90c236ad1ffb5e949869f8a6401df39b9e2`  
		Last Modified: Wed, 20 May 2026 21:16:19 GMT  
		Size: 9.1 KB (9138 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:82dcdefac0d377dfdd71081dc2d0e329261a5d5d617e7ed2a9b120af621e218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158326662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ea4f935f7c911b4c8937aa1eec3aa801be78cfd82912159be0bbb1d8902a59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:56 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:56 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:28:56 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8f4597ed0e7e7fd77b2efad016d94d0a784114b062f73558809c1aa0b8c95`  
		Last Modified: Wed, 20 May 2026 21:29:12 GMT  
		Size: 91.4 MB (91356493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:15ce87c6af5c5de9985c880743891ef9fcb3d0063029c3a6ae2bba726ca056e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a91a4bd7bc1d42a151df4d4cfcbc15d4a6e6580551191fab2fb09a72ecadb8`

```dockerfile
```

-	Layers:
	-	`sha256:970d7f1be76224ee143c2a28489c38d82a130f2fd2bbb346d6761dffd15a2011`  
		Last Modified: Wed, 20 May 2026 21:29:09 GMT  
		Size: 9.2 KB (9230 bytes)  
		MIME: application/vnd.in-toto+json
