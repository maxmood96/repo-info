## `azul-zulu:8-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:4de4727aa2ca2e73e10c8fdaf327a8b148e04a1570c6c814fa8ca8ac0ca8615e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3594d6caecdab7136cefd7047c1a79d95c0cb101d2585a2e93dcf382f01b19de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128565407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283df87df9821813c90460847c16fcb6afc505c2328b8a2eb539c56dcef85efc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:33 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:33 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 26 May 2026 19:17:33 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534791b5e19dd9f64cf58ef1756bc43015e7456833dec2d2aaa1639461e36c37`  
		Last Modified: Tue, 26 May 2026 19:17:43 GMT  
		Size: 60.1 MB (60109370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6fa642c5b5f5175bac6665aac2875ac33151c8a1486cecc4d8f4b17b0413d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b20fb410d77df1a2d3af4c7cb35959d7422408bd15f8da61b65be77cfdad48`

```dockerfile
```

-	Layers:
	-	`sha256:faddeed3728407ce3433d386d31ed1deb8ddc51456844f0a39bc7d42eaa106b7`  
		Last Modified: Tue, 26 May 2026 19:17:41 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:839a83d9109fd52f8c29c2b6d45af80d18774df58a42dcf517998b5861b86e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137044702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d071cafe6fe382dfc3823b31e12ee7e3804edbde3abe3735821b677b96cabcc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jdk-headless-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 26 May 2026 19:17:39 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb9aaa40e8232edce7945eb0b6db1c713fdf1c35123a369c67612850aaf20f3`  
		Last Modified: Tue, 26 May 2026 19:17:48 GMT  
		Size: 70.1 MB (70073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ee5efe195a4f33a7d0bf355561b830bc0b27e74fc3dbd72eb9743750c8986f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee524d27d6bd5e22c20faf3fb4835ae06b0dc66af0492966996868c4210ea838`

```dockerfile
```

-	Layers:
	-	`sha256:a0fa787e1d162b2b8ed636d832dade274fdac39e97629a71ec658a8fc8e3bedf`  
		Last Modified: Tue, 26 May 2026 19:17:46 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json
