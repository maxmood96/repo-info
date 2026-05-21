## `azul-zulu:21-almalinux10`

```console
$ docker pull azul-zulu@sha256:503025929e1406fa277b0f2a068aa5710134be49cf63ceada4063e07297f1b42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:71566bf3a57f4528a63c7dd34e2d30f9fefe5b932defba0cc5789d4b9dc8be50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233925172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11230ff407a404cfa406c8a12cc2f9d0800a89842ebdb78d31fb3dbb72dd6b06`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:24 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:24 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:15:24 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:15:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788b12d3ce79727fa544522d8f078e274e29fc84385c0512fdf307188b89d120`  
		Last Modified: Wed, 20 May 2026 21:15:42 GMT  
		Size: 165.5 MB (165468570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d92d5144cd847d9067c167744ce379c5bd48c8ff436374b11bf0c8cf15ee3236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd732a129cc5a43500f22316ed84ec0dd54015a78044251fafa036428d581270`

```dockerfile
```

-	Layers:
	-	`sha256:2d6411d1d539591e10cda0a7cf8e42ec87975a45fe464dcf3d24c83e242cbb08`  
		Last Modified: Wed, 20 May 2026 21:15:36 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7009dc1b88c791eda435fbd6251bbdbc8be05c9bd0392b473a5d649f3c17d347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231755723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7251debec81ce4d3ebb3c9d41d16f724ef9af17d3254ea59ea12e731ca98f0af`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:16 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:28:16 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:28:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8524e8196337bdc90a41965c781dea0e7f46fb1a432eb842acba118883370`  
		Last Modified: Wed, 20 May 2026 21:28:33 GMT  
		Size: 164.8 MB (164785554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7998a2cb657047fc67b5afb4d4e3bfa5b6ba19607fe9b876ed270c5c5630f9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18e5cef3173cecc6b4e89049f6ab925a4c50525a3345f4208a37328ba72d406`

```dockerfile
```

-	Layers:
	-	`sha256:232bd45c544338e4f604f745eef5baab40949dd73fa4166fe550558ad7a96348`  
		Last Modified: Wed, 20 May 2026 21:28:29 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json
