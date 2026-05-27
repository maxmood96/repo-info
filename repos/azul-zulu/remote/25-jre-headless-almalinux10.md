## `azul-zulu:25-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:66d6caaf7303ac044ede88c1d1d8c23d55a0e050b913037d1fe45c42b251f3b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:8bd5694f0ab6b282e7b04f302e2319923744fe6cb9f51ac0847b795f98b4a165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158439020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcb7383ee49246736989885c968f0fba7b55bcf576bbef78e733a0b278ebe3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:46 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 27 May 2026 00:19:46 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9b6a5f0db1ff903472778ca665880b2191376d5ed546e7a3039fc5935203a`  
		Last Modified: Wed, 27 May 2026 00:20:00 GMT  
		Size: 89.9 MB (89878707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ec7c121827556cce139ae9bbafd5e8efcf36123fd5071650c0fef6989565bb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d356466b6193d2b2906abd172346d24fb694dde80a7d743242a4fd1bd798671a`

```dockerfile
```

-	Layers:
	-	`sha256:d417bcdfafd5e4d5d70891ff84bad4f95072a0dceb7662a98353794e14f7f5dd`  
		Last Modified: Wed, 27 May 2026 00:19:58 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:36109deb31aa6c4adaed0eeb7f2aa35d4d0f515b5faaaf15d90900933c0fbaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156609377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff24b5f1e566753031f952e478189450ddfe22fedd225933aaaa6f7a0713639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:00 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:00 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:00 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 27 May 2026 00:19:00 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3642fac1cddf9df73e15bb29df4255a94d20f02696eeffd1f2052291a6fdd578`  
		Last Modified: Wed, 27 May 2026 00:19:14 GMT  
		Size: 89.5 MB (89477643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:600161c354441e1e6245ae88525b72cf00fd71e1b09927095cde6bbb1163857a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1f5a74054ba7dbb0a6736022ab883212bde7ecde7fa783a6380680dd804fd5`

```dockerfile
```

-	Layers:
	-	`sha256:d4ee58933edb593fc2f35a7489809d033ec1c6e3854d0904599e8ad267044ddb`  
		Last Modified: Wed, 27 May 2026 00:19:12 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
