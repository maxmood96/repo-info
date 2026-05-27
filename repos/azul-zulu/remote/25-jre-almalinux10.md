## `azul-zulu:25-jre-almalinux10`

```console
$ docker pull azul-zulu@sha256:e89c3aff14eaf3c0e8d9151b44b25b9bb2c374426b7c606fb98dd29474598f8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:949a230bc98df031894efdae02375b1a0351348b9e7cf3a34f453d83e2488c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158859116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d775ecb222832e431e5f5376c719dc6ca6a3c114017a70cb8750cd016b75342`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:32 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 27 May 2026 00:19:32 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10f889fa53d9fc6b6efb44723ca730b3562c12d45500105d2090ec1c75b14b`  
		Last Modified: Wed, 27 May 2026 00:19:47 GMT  
		Size: 90.3 MB (90298803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a57e5e6254067ce206b40abed18de79e97a217414b77bf9a1ebcf33addfb7347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69726b2d8dc133950fc69e54d5ad62626593936b2799e1a1e41f5cc871b0dd5c`

```dockerfile
```

-	Layers:
	-	`sha256:c4dd0ccbdeac5998fe78469258cda1026f90f95c7da51c7251d81190fde70ab8`  
		Last Modified: Wed, 27 May 2026 00:19:44 GMT  
		Size: 9.1 KB (9138 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ebd3b562afd951c60c7ceb8f089b7f15d03c01ab59c286aa3e5c3140366af524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157033960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ef20bb2404e0cfad5d92bf2614d02d3ee6a0f999d77441f180e69904f210f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:00 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:00 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:00 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 27 May 2026 00:19:00 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b3321b969dfbc1d79f59d7892f91c95cf9128c37dd7f9b7e9ad1d0614e147a`  
		Last Modified: Wed, 27 May 2026 00:19:14 GMT  
		Size: 89.9 MB (89902226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0ae117ed561315ddec88864360317543a98727997a1c9d8d7234395e4c2238e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff98b1a7e1518d47904121cd543ca19093ad959f0528559d80b45ce1680ea6`

```dockerfile
```

-	Layers:
	-	`sha256:08f2975b367dd3298ae26fd3175a48cd2db63c3a3ee2d58670efaaa427e8dee5`  
		Last Modified: Wed, 27 May 2026 00:19:12 GMT  
		Size: 9.2 KB (9229 bytes)  
		MIME: application/vnd.in-toto+json
