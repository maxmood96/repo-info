## `azul-zulu:11-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:dd093f5f1e52fb10616c728a12723c5a8e8ddc537aa1d0c556b80858896e70d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ff7a64796e511d9a8094229e62389cf80e1baeb474e5fdfd372661865c4c1f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134933593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b6d01f8a322273bcbf90d3d15c205818567ec0195025fba62dae512138e344`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:41 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:41 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:07:41 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8886a7d2776ca40390b6de8c4c91c78fb486e846a6062e002f58f09693f19`  
		Last Modified: Tue, 02 Jun 2026 19:07:52 GMT  
		Size: 66.4 MB (66371131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3fae759098694536442a79a8732011a879eba1e22b82e0d92f6051ea74f6d1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e500b7efe1c4233b1fb4bb66673a24b517186f6055d83f59bc657535cb2bace2`

```dockerfile
```

-	Layers:
	-	`sha256:aea0bf9216f31fb34da0e31ec96a095d08cc918e1bcb10c981390948880a287b`  
		Last Modified: Tue, 02 Jun 2026 19:07:50 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:997a59258f00760154d6b3776c4e7a7af2a60e8b2459d2397c4ae2522df79fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133333781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31355866cd27c26091e2d38296e20765c39a61205f868328d4381b7d8fa1c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:02 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:02 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 02 Jun 2026 19:08:02 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5b5ae5330424227c83d98115d1eb9c1607339cbf3739eb30981ae2c9e1890b`  
		Last Modified: Tue, 02 Jun 2026 19:08:13 GMT  
		Size: 66.2 MB (66191820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c39dfe5ab92444424caa4a56fcb5c3e6ad12faded2e242a00559899d0fdc24e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54930a6015234f5d7f9c09111f11f0f38b848f9643254d96be68e0284af484`

```dockerfile
```

-	Layers:
	-	`sha256:12f2f8654889934473b2a4e7801ec656b5ddd32f71bf2141863aad7072095f3c`  
		Last Modified: Tue, 02 Jun 2026 19:08:11 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
