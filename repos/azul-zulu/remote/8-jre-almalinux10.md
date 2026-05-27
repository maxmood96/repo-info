## `azul-zulu:8-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:4971f42b72c10cd9765a8914e8191fe88f2ef515f6e2693ecf2c0fb248de8be5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a39ae2322ac47fd5a4d0da1baef23a6a21c5b683dcfe391a630ba60f70d1b44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119758034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c6ddfb86a9ce89ff011c24df42dd8cdcc5d336ec068f2691294bf9a8489e7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:25 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:25 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 27 May 2026 00:18:25 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dc930efa88e320bcd857cc027b6b597ace4aea41270130757b035f3953094b`  
		Last Modified: Wed, 27 May 2026 00:18:34 GMT  
		Size: 51.2 MB (51197721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:55a27a90e918a8131e2941499d4dda2581b5bac2d5f94be0db1318d92a4f9986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7c58f01ae275a79f51c860978ff628a6cb0c2e2cb11007b86b7597135b3c7c`

```dockerfile
```

-	Layers:
	-	`sha256:7349ef5c8f27801f80f11ef5d82c535ccf0f43129b33e6cb5f1b771e335bca72`  
		Last Modified: Wed, 27 May 2026 00:18:32 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7757112b0c8a54f94382116f7dfa6b07cec4588d0d569c8302b780e940b685a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126609508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d291ffbf93ee7df201729aa9b075322c7294a2188604182fd44d9d3362bcfb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:02 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:02 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu8-jre-8.0.492-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Wed, 27 May 2026 00:18:02 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280af5510808cf3a7151567eb8a73f87cb4dab445c043a9ae1f40813c7b77513`  
		Last Modified: Wed, 27 May 2026 00:18:11 GMT  
		Size: 59.5 MB (59477774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f57f0a5fcbb6c3e2b0a8118d1ae699dff3a1ccadcc704773a1f406e628c37d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36b491e3ee06f683c65e38603a0f5246a217829c6e0e4c128653384cd1bcaf4`

```dockerfile
```

-	Layers:
	-	`sha256:2f911b4abacbdbd0fc7762ede4ea3a872fce0745bc0e3e0baf480af84c2b4b40`  
		Last Modified: Wed, 27 May 2026 00:18:08 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json
