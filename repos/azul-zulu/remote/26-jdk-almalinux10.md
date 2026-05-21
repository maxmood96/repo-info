## `azul-zulu:26-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:1598b446b81042e84f358ff9f9ff7d233b276bfee4e8401d269da8343dbcaa4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:fdf757c6fbf087e7ff1a22a3401dc5b2031911b93a0a5fa876b82f3a22e4fae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255260022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e8b803b7ef20f8c23515fef61c6037acae5ba2e415469e7ec7bc5795044a4a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:16:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:16:08 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:16:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:16:08 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:16:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee73985fa81e4e8bf9de68903dbc9ef3470e50d5103cbb587d14d335b4acca59`  
		Last Modified: Wed, 20 May 2026 21:16:28 GMT  
		Size: 186.8 MB (186803420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d554d54a60478ef3b9f106054a2f0a4a1ee775c1c88e7dea9614b7bac815d406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b9743d0cd4421e35f00d2dc8830a7a47d23bea6fbf065949a869fa64887a2`

```dockerfile
```

-	Layers:
	-	`sha256:9726af9f554097aa47d71f674d27ae01dc852b19e1c249fdaf64bd2b4176717d`  
		Last Modified: Wed, 20 May 2026 21:16:23 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b4ecdff1ec77c1d40ad1705bb47013f8411d5b8b186204a41f00f5f8ae723983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253475034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b66695f44cee1e0deacb3c6c9ad9eaf45e3708bff5a74b468c2f88f59ef166b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:29:01 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:29:01 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:29:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jdk-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 20 May 2026 21:29:01 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:29:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0756e873a809abf5616026cf819e8eb0d5dcd30d41614c21cbef80418572e`  
		Last Modified: Wed, 20 May 2026 21:29:21 GMT  
		Size: 186.5 MB (186504865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:79b562262cb110ef789af2cf13e839a213dee02659d82b60390df7bc975073dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475475abfc423d03cb3d6d0572b7205cc03218b3a07b427a3aefc6e023a05f70`

```dockerfile
```

-	Layers:
	-	`sha256:95c7221368a39c9d3ca99c6842ad5fcd1aa054f2a35fd6bcb1c75a01bc25a3e3`  
		Last Modified: Wed, 20 May 2026 21:29:16 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.in-toto+json
