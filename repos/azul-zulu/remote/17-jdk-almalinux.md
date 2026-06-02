## `azul-zulu:17-jdk-almalinux`

```console
$ docker pull azul-zulu@sha256:30a4a58ea9c7a77f7c9840aef590bcc99a9aee44b14afd5dcc1827b8ec0b0f82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7ad68be78435a46a8ef3f97d2b357d520da986f9fa73d91797339dafb1e3a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220684645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b9dd653a9f535c4c2f15f70396c74f53fe0a3b37cedffd040f0079a428a765`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:52 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:07:52 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:07:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3d18e996b1a62923e29b8e3386b47e5dd5eb3c04c1ffe894342f9351a64bbd`  
		Last Modified: Tue, 02 Jun 2026 19:08:08 GMT  
		Size: 152.1 MB (152122183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fc1109672d87d6ba6b655ea3d5b48ced0f81a83acbbbf80cf41f05e4547d10eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3c5c448b23de476675f2cac5853af2e1114cc109100188fa988473dbd07972`

```dockerfile
```

-	Layers:
	-	`sha256:68a093fdd1105b117fe851a02d681c416b57697d29b1ef7fd4be397beffe1db9`  
		Last Modified: Tue, 02 Jun 2026 19:08:04 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ef3768f5c9786bed51a36fde34501d21f5bc9b32e56b9591a051ee0c4ee59eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219292640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc9308fb78f0c9db8c803ffd8adfee1b17ffbf280c9e5885673a317670e055`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:10 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:10 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:08:10 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:08:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcadc851bc59cdcbb04c3e60bfbb7bab9dbbffe4a61a73b21e2bc7b39fd0c04`  
		Last Modified: Tue, 02 Jun 2026 19:08:26 GMT  
		Size: 152.2 MB (152150679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1f765ee7ea47c825cda96c91fd16d935f82623889f8fb587c990ad026073f735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4553a9b5056e71818a1324af226c28afe6af70174748d7371a0ecd32c0a054`

```dockerfile
```

-	Layers:
	-	`sha256:40531d348faa1b471a076eacebf5e560778c0e6333d3375307b248f7f6429c21`  
		Last Modified: Tue, 02 Jun 2026 19:08:23 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json
