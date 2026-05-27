## `azul-zulu:17-jre-almalinux`

```console
$ docker pull azul-zulu@sha256:e2a0c7f7cc3a8eb4ccf35e538f9129e3f40318a138ade0a75dc81b716560bca0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c5e436f869a0e8dc47a153fe31d4de2c82689bbbe28763c01d1f5a81c36c594f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139430682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1080c7fb02444774897893f859cb7c8fe1feb9fa0fc792e27286143fb71dc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:52 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:52 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 27 May 2026 00:18:52 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb06b56080fb11fd0acdc3c417b83b4570525fbd55064153609cd1c05ba7503`  
		Last Modified: Wed, 27 May 2026 00:19:05 GMT  
		Size: 70.9 MB (70870369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:214bc4da4c4ac45b7df7f0adb1f2be4eef4e04adcb2707fe150bcac2ec223c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f946acdaff7a7452eac7fb1770625c3ef5fb23a63872686e3bfdb9d3425f0b77`

```dockerfile
```

-	Layers:
	-	`sha256:844ab1cb22d4e36f22feb1102b87e8b6ebd15e3ce9fc1d6496813c1e88c6e3dd`  
		Last Modified: Wed, 27 May 2026 00:19:02 GMT  
		Size: 9.1 KB (9140 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c8110cd51a2a0aeaaaff6e7ee70471b8602d822e6c5932309167046b082ce929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138050646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62efdba1b999c11028629ef12fc70d10f01c63bc232a28d6e5d8a5402ede190e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:28 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:28 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:28 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jre-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 27 May 2026 00:18:28 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72a3d30e6e20f749bd8637bd12889d9cf85467b46b2f53e3f757096ff3e2933`  
		Last Modified: Wed, 27 May 2026 00:18:40 GMT  
		Size: 70.9 MB (70918912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:eb03657044e1a1aef3e17917257fe15b6f07fce031993c21204436490f772d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abfa20e3ed6f8c991d4cc80b5826a251596beeede688647a78e1775249de42d`

```dockerfile
```

-	Layers:
	-	`sha256:4fd1b3f7a10e028c9f3d5d2c888884875c74a1df259ca6485d9c1dbe406266c4`  
		Last Modified: Wed, 27 May 2026 00:18:38 GMT  
		Size: 9.2 KB (9233 bytes)  
		MIME: application/vnd.in-toto+json
