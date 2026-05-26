## `azul-zulu:17-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:43d6c7577e0aa9fd0e93282abde8f96fd5787eeab0d1bd32e1c1ca1da7c639ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3b5c452fc31c6b7ed8ed85bac6d3984bef0a3f10607544e4b4ddf4a5927e796f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139376947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b23cc79834beaa38b62c598ffeed13fff28367b2172b8701f42ef16a15c3fea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:03 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:03 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 26 May 2026 19:18:03 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a036933b7ffb1a9cc8e39e1d1c06d6283f9b1d1ff08f5cc2af02ca75895a271b`  
		Last Modified: Tue, 26 May 2026 19:18:15 GMT  
		Size: 70.9 MB (70920910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c8d9d5108b1268cd0b59984b5a403bd7c7dd9c48ff2eb34525c4fb0f82a7a5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46a9b21ca53c6e4d9b9eb2b84a4897478f5ee824dd94532391d648b22290c49`

```dockerfile
```

-	Layers:
	-	`sha256:1dbb4a79593efa76ae441d655259c883b82c666a35aa1f6ce38020fc0ee78d94`  
		Last Modified: Tue, 26 May 2026 19:18:12 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:abc1c4f48e05e8907a8db55287cab7fa1aa2537254ed696c2ee32315d8224810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137948772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a483d1e0224a1214e9d90f2d8b0f907ebdbf6462acb444e7627be894b50ab91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:19 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:19 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 26 May 2026 19:18:19 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c23b43f890aeeedd57954bb56ea0c347b62d7f6356313dbd092f130d8837b9`  
		Last Modified: Tue, 26 May 2026 19:18:31 GMT  
		Size: 71.0 MB (70977880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:49b41393c3c010e2bcc3e11a05f51bfb10332461b20f4e9fa914f2879bc477af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9705fa0221b169f01200cc7a47d4a3df0f87f0773173334a15b0107dd0a049c`

```dockerfile
```

-	Layers:
	-	`sha256:3fc332d33a25eca8141f07ab4e5085d7f3804e53337fb1317830e9b7ee072351`  
		Last Modified: Tue, 26 May 2026 19:18:29 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
