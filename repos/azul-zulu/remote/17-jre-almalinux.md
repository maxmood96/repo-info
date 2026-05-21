## `azul-zulu:17-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:a7778f41ad68e65869c055897665b634d81d03edd8a27ce077676135be4ce176
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:dcc3c09bb779cee91dddc00bc4ebdabedf5f827c05811131f9b894a36de8ef63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139375069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de67d48f99add7447be741ca831bd11eb24e8ca635c2c8e3862864b18acaa4fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:01 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:01 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 20 May 2026 21:15:01 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4504638a304592562f1c2db993e29cb16a3f242cb9633a01a21b89a459b0591e`  
		Last Modified: Wed, 20 May 2026 21:15:13 GMT  
		Size: 70.9 MB (70918467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8d8a7615aed2a3069f1f6e7e57c701e73c0da954c706cbf042e7ebae4d380bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe381d77ac3719bf1089511896a171741827de6ec94d6f6f9b4b7cfcc0593776`

```dockerfile
```

-	Layers:
	-	`sha256:4a4ecc57921ee952d7e5736c0f2a8a25da0d61ba6e2600152e54f1e42bdcb7d9`  
		Last Modified: Wed, 20 May 2026 21:15:10 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:54f2e8b6675ec1af4c72892ab707ee283b77bdb7b6c2a3706310313404945b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137946247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684f800aa52ef874a057bb8c5c78ddcf929737a6a90d4703b3e6ce6249f2cd58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:27:45 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:27:45 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:27:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:27:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 20 May 2026 21:27:45 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0996e9a936154054f43333ce81a243b32c22332aeb060b2d14ded686114419`  
		Last Modified: Wed, 20 May 2026 21:27:58 GMT  
		Size: 71.0 MB (70976078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3f5db421f413b1821896aa004f6ecfdbee757709ea4c9e436bd9a1bef860f356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e83c14776737286c150710dc7f35b0bc11fa74ab6b690fd0859a72528bfcea1`

```dockerfile
```

-	Layers:
	-	`sha256:319c896b0f3a4b4f04d5520128bf9f8c7c131a89d08a0f97b7b77b941bfa1567`  
		Last Modified: Wed, 20 May 2026 21:27:55 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json
