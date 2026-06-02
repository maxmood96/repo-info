## `azul-zulu:21-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:8fb2262f160951b61af888427816ec45b6c21efc223792b558ed3f115bc70940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:61ac3942c03eb7b2f783882a35f78588e80e530c6fbc3a24b74ae17c3ae4036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144713155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958ad7cd16a1741dd816378121ec6e342503d2188e5a4b376ec02cbb946180f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:06 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b6ec8dc01d89053fb0b90062dc0756ffdfdb50f2a1cc777318a498826d6b44`  
		Last Modified: Tue, 02 Jun 2026 19:08:19 GMT  
		Size: 76.2 MB (76150693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:66cfd5b3676fac3fa12c9cbc5df303ada9a972068d3403bd81c5ae9e9582d0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3770bef42be0c31e94c9862949c78af56aa088ef6362364e210fba1978637ac3`

```dockerfile
```

-	Layers:
	-	`sha256:d5c70f52fcf2f922a3642c34c24a6db8fb01c56535e2338bac2781d49dc3c938`  
		Last Modified: Tue, 02 Jun 2026 19:08:16 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d3a4d512aec194d5c040f563f1312b17b7be236345c98af62c6b4d3bf5d42621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142959120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aa366c01943867a89c54c2b20bc02690ed1148fc05cebb7eea5c698eb0074b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:25 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df072b18ee336fe908fd93812a635be2b9a4925d47b873a88637f76c7f0d5c7e`  
		Last Modified: Tue, 02 Jun 2026 19:08:38 GMT  
		Size: 75.8 MB (75817159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e3af755e7e3022b1b308153c93fb48ea4372e136fded0aecc2120b35cbe382cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817fb1ebe48648bbf61ac7d171258f926b8a90ea9f8a1879c9b2c0015b177c24`

```dockerfile
```

-	Layers:
	-	`sha256:122d148a05adb7a59f990bf9f8f4356b3300365f49ba6c3b9b8b47b0ba2ce2b8`  
		Last Modified: Tue, 02 Jun 2026 19:08:36 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
