## `azul-zulu:8-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:a874d7a7aef4f3bde34f51e0bd7e2791a8bc2a24359b5941c76e16d113cd97e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b6a057f83417fa08ae808e6ea7c5007ca0774527eef58b42964f62c858a274af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119763239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a1d2486ff93a1bda079c6e9f6d4ae21747da1371bc26187610671daa659e0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:17 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 02 Jun 2026 19:07:17 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0dbd8ca8db6d3a0d16627d99c16d33b0a4f391696dbac13a71ce9680429bd7`  
		Last Modified: Tue, 02 Jun 2026 19:07:25 GMT  
		Size: 51.2 MB (51200777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f81756cc35fa4e049e1ca47e8260e736ad1f71a01cb26c124c2de05a3f7f4708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5b90ce709ca2ffd521a07f76646533b45402e81d6a6f813128019238d4d1ca`

```dockerfile
```

-	Layers:
	-	`sha256:4dcc2cc1085a8dc6bff2a3512b3bb9b6b183ed7e05aec58737c172fc3e51b4d6`  
		Last Modified: Tue, 02 Jun 2026 19:07:23 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:19a4456cd84af75cbfe7490a6b8b23b437317b79eae5480db11e85e240b3ca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126626419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061aa8325a2a2394bfad4e988b8657e6019cb86a4e4b13bc83578bdb0ef0f3ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:07:35 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:07:35 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:07:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:07:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Tue, 02 Jun 2026 19:07:35 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5398c5f33477c19e1f87ab804dfc246250e245a22dd5dfb7021e08e32bf1fd`  
		Last Modified: Tue, 02 Jun 2026 19:07:44 GMT  
		Size: 59.5 MB (59484458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1f75c8a072acc4d6317198a3a4f4b49e33c0b394e8d118bc72c075c8208f454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b2869d60489d5bf68e41fa13151fc604a1b78d675544c341c66fd83d2f5e17`

```dockerfile
```

-	Layers:
	-	`sha256:b5ceb47fbea922ab58dcceda004d1738fbc3ff62086538911cfc8a7084ead33a`  
		Last Modified: Tue, 02 Jun 2026 19:07:42 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json
