## `azul-zulu:26-jre-headless-almalinux`

```console
$ docker pull azul-zulu@sha256:8b2a4c3d52b33efa581c6389f6c2b672c2a62da9c4c7d51a6bcc15d1379f4ce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:16992f8088e8d7ec4b7bd88087606795893d2b393a09a7c66ced84156a1b0fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159524232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ec8944334c52741c9eb42baf33ad45bdb3ccb229dbeca2e2aab060570cf993`
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
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
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
	-	`sha256:8745231f5fc71f0a0875a460e43e3c855b6b0b54bd2a1c1116b1631ba8c80e3d`  
		Last Modified: Wed, 20 May 2026 21:16:22 GMT  
		Size: 91.1 MB (91067630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3df58fe93fbdfa347e0aacac8275ab454b52f34181f9e54660867f940407c742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dba93dc812a03b159c7bc5075b02172a7d8c149316d21c27a4cbb1527c8c030`

```dockerfile
```

-	Layers:
	-	`sha256:90e50fe208070afb75263586ef4dca395cb17be77b1bd0d66dc8cc53f3c3612e`  
		Last Modified: Wed, 20 May 2026 21:16:18 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c7b83e5426fe33a455819570d3f078654acb188a4602e58b7ae2ee606a27eaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157967212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec0913255e6886325b74a20edcd34f9aa2e962a59de4d895eaad934f9903750`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:29:03 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:29:03 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:29:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-headless-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:29:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:29:03 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0007681c1e70d8fe140242e69ffeb438bfde118c3f8bff3a0a879798116fdb`  
		Last Modified: Wed, 20 May 2026 21:29:18 GMT  
		Size: 91.0 MB (90997043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:49d989f89207a34063d63e142247e3eb4fa251eb7bdaa1ec3ca2026e28c03906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990809910d1f68c4f7c6e773a5a37d37c7bcf27a1bcf8bea6f51f953847ac37`

```dockerfile
```

-	Layers:
	-	`sha256:60a7812ec5f2ead9a74a90d91e226995a0b3bdca2db817c68b6a259376426035`  
		Last Modified: Wed, 20 May 2026 21:29:16 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
