## `azul-zulu:11-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:d9bc42dc732b7c3b8776270f86f1f40bdd72a74df33c003a6461aff2963abec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:0bd7311065a285e03623fb69ec811c807f4e96b5c80912c1f98be1d37f3c72f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134447039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfe307f3a35ef2e17ee57d408c8e5459d1ffcc656b8271d5ce214b211bd435e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:12:04 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 26 May 2026 19:12:04 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:17:58 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:17:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:17:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 26 May 2026 19:17:58 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e00696cab286036acbc1819dc14bffffe3d9b62859baec766357c34271aa510c`  
		Last Modified: Tue, 26 May 2026 19:12:20 GMT  
		Size: 68.5 MB (68456037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4453ef626885ec74d73938e7ee0ae5201413018415165ce58b4610c5cbfc5d00`  
		Last Modified: Tue, 26 May 2026 19:18:09 GMT  
		Size: 66.0 MB (65991002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0e1d18c28317fc5bece0d78adf70c9639e506cc7752fc9895face076c36fe784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7fd5a424abef3bc3a6f150c513dfb4735459dddd3c366afc74e5c6b7e553e`

```dockerfile
```

-	Layers:
	-	`sha256:c3de0c3c3bfa6eefe3e2787d12d586366230881bed8d8096f4015c83b9c3e4be`  
		Last Modified: Tue, 26 May 2026 19:18:06 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c2f69c5fca26bf7cfb3175ff51eea58247fe36f4155338a8b0a54cfa520f7420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132791619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfa1b83b94957f8a7b67babab915a9862cf9f6222053417b260337811bb99de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 May 2026 19:15:08 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 26 May 2026 19:15:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:18:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 26 May 2026 19:18:06 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:18:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jre-headless-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 26 May 2026 19:18:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 26 May 2026 19:18:06 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:b1228b076bddc8d6b69c35f53b57866988d02e0877190f42b0390db4a24d6bba`  
		Last Modified: Tue, 26 May 2026 19:15:24 GMT  
		Size: 67.0 MB (66970892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0044f3a531f607956aa2432be195e77c101ba1776ae6bd3f856d3a6bb523c5e`  
		Last Modified: Tue, 26 May 2026 19:18:17 GMT  
		Size: 65.8 MB (65820727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:57d4225cde9e4ad6f59351a5fbbfa679328b6f73d76c9816587900d08e81fe75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713beef05f8328538ac464fc0b20ed337ef41aab1e447d8943171b1d53a17c8a`

```dockerfile
```

-	Layers:
	-	`sha256:f8aa929db18659d84e55db5e64d2951733318b883009e5e015e8f397a002c4df`  
		Last Modified: Tue, 26 May 2026 19:18:15 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json
