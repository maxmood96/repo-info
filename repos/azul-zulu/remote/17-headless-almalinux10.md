## `azul-zulu:17-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:154162a0ced874aec4d7a0507b151aaf8a02d6786d9ee5dddd02903868c35cb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:17d942164aa8cc9f2495dfffbb48ae868d08fb61f6984e1189955d83b3076bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220002083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d29b73b064ba4b06f85b294be4621214a1216778eab70eb34ddf27c3bc5519`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:53 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-headless-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:07:53 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e35f3d3eb7fe1f7e6e35c1534e0ec45c0a6aafab4c433c4634fc81a6b3115`  
		Last Modified: Tue, 02 Jun 2026 19:08:09 GMT  
		Size: 151.4 MB (151439621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f2317ec41235600cd2d7a0f1baec9525407e094e158472a85bd633d7a6bd5053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7502ce0d4bc7db8d029e8ffec37bc8f1802be77a68d3f477acf8bdf8e8193b21`

```dockerfile
```

-	Layers:
	-	`sha256:1c90e9685e9a81b56fd969157067bb7c99862abf21740d54b2711a3ec94011ad`  
		Last Modified: Tue, 02 Jun 2026 19:08:06 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e1a6c9ce85badd3fc353b9c20419b778214290f4abf840fcdfcf2ca4f1d029be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218611809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d2581467c527c3dd7971ae9ef2a509beb60af9236f6f3cf9010d06e7976b4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:13 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:13 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:13 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-headless-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:08:13 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87eedf153fb458e29042cf3efa7ad53d5092cd3840e325529c2988f735f102f`  
		Last Modified: Tue, 02 Jun 2026 19:08:29 GMT  
		Size: 151.5 MB (151469848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1d9a2cbde89eb9f1f1d1a8cf00a9fe9f92df9b6977243017fc2f3312c45de7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1d578a0c76547087dac18b6d53272f896098682565331dd873ad1f595587dd`

```dockerfile
```

-	Layers:
	-	`sha256:c53c9a2ebca92b18ff3f0ed08d4051297ea5a51932e38d9092089050f0ebc80f`  
		Last Modified: Tue, 02 Jun 2026 19:08:25 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
