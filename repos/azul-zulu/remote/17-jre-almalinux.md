## `azul-zulu:17-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:c651b8ea4efe289d15fb6cbb1073ded8b2cb84810442270a6a363b1a9b731a50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3b7f216d488de81bc9495c50f8b48bf265e50ea276523b2c14fdb6b37b7c941b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4ce42f1643849e7191788089a60bf424b29063a6e2b59b7d11c30064adfe6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:59 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:07:59 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98546bdc6036006f5e6cf52f6926f14ef6222b3522368a7184d8ddb95bf85302`  
		Last Modified: Tue, 02 Jun 2026 19:08:11 GMT  
		Size: 70.9 MB (70871799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ea41e0d299cf49f3c3fc15c6f2a9723ce8af366e47ded94a154a68fb85da7315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89579320e9feaf756a4dba4df42756f56106ce3ea8b3ad24079acda34aaa42a3`

```dockerfile
```

-	Layers:
	-	`sha256:df957aed549a598f120bd6df1349f2de91794a3440aaf769acc22d1cc3b39e28`  
		Last Modified: Tue, 02 Jun 2026 19:08:09 GMT  
		Size: 9.1 KB (9141 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e5e7978d7d74eedb5d72419cf90afc9ff4207380dce6dd2d17040b577eebc019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138071485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e151ed54ffa44d5fb2b3bc1325ff73c5cdbfda1328f8e4f3fbf6ec990178a28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:22 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:22 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 02 Jun 2026 19:08:22 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4926cf4967733b75126e5d800b2ef057c1f7ca4d23d0c008acdd7a72c01a7a69`  
		Last Modified: Tue, 02 Jun 2026 19:08:35 GMT  
		Size: 70.9 MB (70929524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3575e4bc0ef96991fa3c25455cb770f3a178f980c6476226b5cc9fe1b0b0ef5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3711894ccb4c75033aa3ff5f70d08a1bc908e42fee19701756ea94ce381ca9`

```dockerfile
```

-	Layers:
	-	`sha256:0c00b935e6632921cfa4369652a8d380c506b239b6f3ac267ae38d7648f2167b`  
		Last Modified: Tue, 02 Jun 2026 19:08:31 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
