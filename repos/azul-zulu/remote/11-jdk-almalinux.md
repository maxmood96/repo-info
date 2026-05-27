## `azul-zulu:11-jdk-almalinux`

```console
$ docker pull azul-zulu@sha256:b6c161ce73faa855a55d11df9a23c2617428661ccac0226e00e9b36118366a56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-almalinux` - linux; amd64

```console
$ docker pull azul-zulu@sha256:354c95fe10ef252450566ea2063e4c35ed0d761622f6ea4181eb023327d9e464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216522768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9757d16f8d0e7590545517b288522036e194c540e7f964a896784fb0238266`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:34 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:34 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4610f03d0460e19afc8a0552b3507845948d67df9262beeccdbd37f9a742a4b3`  
		Last Modified: Wed, 27 May 2026 00:18:49 GMT  
		Size: 148.0 MB (147962455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cccf62c0555e5e59ae1469289d97c08c0aa6f33e915baf10b490e7657e5b0f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b491a08ffa57235ed3b1619ecb3483bc6d8c0747facfa3ff834d2ef4c05ede7`

```dockerfile
```

-	Layers:
	-	`sha256:d37e331ef8e0738be159d7152139488b8bc405ffa0a5677c8500b3da1d97ddbf`  
		Last Modified: Wed, 27 May 2026 00:18:46 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-almalinux` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:32a12fc595fd1fd259fc252efbb13d1cadffca0adfae7ce27dc3e6f4716b7b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214786042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744ed78980f153f40e953527965af20099930afccc794e739155ccb074da89e4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:11 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:11 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu11-jdk-11.0.31-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 27 May 2026 00:18:11 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1a8b198a6bdfe75bfd76d2c3cd3af041b81c79b18dee3a699cf867cce98bf2`  
		Last Modified: Wed, 27 May 2026 00:18:26 GMT  
		Size: 147.7 MB (147654308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-almalinux` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:47e84512747ac0086a8d715c4dcf5929c4b54c633e18de6da58082d4aee05815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300da8adf417d2baac11e1f396e9bcfd20e451e21e64b6f070589b886f4af15a`

```dockerfile
```

-	Layers:
	-	`sha256:1da726972c33863f51992545f0f94ce7e5d6e36df4fa2dc32604bf62c6ea495c`  
		Last Modified: Wed, 27 May 2026 00:18:22 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
