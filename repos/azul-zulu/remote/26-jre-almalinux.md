## `azul-zulu:26-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:964bffd72be0eef20f9b8191eabf86a783d8f3c1bd99f504db11ecfdde4b3960
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1bcaa3c64ef32f3cd4407b1a98a2255e8ad2f35669d096c6933f4df0af581ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159949432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c472fc255f39acaa6929afb3b4e9c7bac9e5c5f16cee85c6e40b019085b56144`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:38 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:38 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:08:38 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eacd62040caa376c7355041efe947a2dae6b77e8e1c3dca9670834d36a2ef7`  
		Last Modified: Tue, 02 Jun 2026 19:08:52 GMT  
		Size: 91.4 MB (91386970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0ea3353be90ec36ea38697acce54607371546faadbc862111fe0af368234575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca63f2a1d6cef5ed680f6ed5f3f7bce6db0bd24918ea2d5f3720dbfcf5045c5c`

```dockerfile
```

-	Layers:
	-	`sha256:7a08808e2e0381ca6293d6691f2a9ba77960b5680d7d31bf50721ebc8f78584b`  
		Last Modified: Tue, 02 Jun 2026 19:08:50 GMT  
		Size: 9.1 KB (9138 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e42cf638f8e77ace208d3eb78200dc3691ab61fab43f8c5171e3912cb67f143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158449584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa4b56b9e880af5575cf8d82c1da9ad937104fd69dcd7bdb9b41afa470f94de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:59 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:59 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu26-jre-26.0.1-1;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 02 Jun 2026 19:08:59 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee57ad3668507332cd3470d8114f904830a09c4a6a620e3cf1ac0860cd83fd65`  
		Last Modified: Tue, 02 Jun 2026 19:09:14 GMT  
		Size: 91.3 MB (91307623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:adc7d20c002aa1d931ea1828bf99332b7c6bffb52106ea26b5236ea63207a06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fcace7809944eeeb59f40124fff794842f0979a67dc56871f56430c90e2e6b`

```dockerfile
```

-	Layers:
	-	`sha256:647b950c35c683aaf33e0281b91e06a8d06ba3ea0d504374900a522d955a34ed`  
		Last Modified: Tue, 02 Jun 2026 19:09:12 GMT  
		Size: 9.2 KB (9228 bytes)  
		MIME: application/vnd.in-toto+json
