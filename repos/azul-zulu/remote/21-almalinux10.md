## `azul-zulu:21-almalinux10`

```console
$ docker pull azul-zulu@sha256:f0b079dca43357623f79c6b141694954f1c203325dd5be97e7cbd9c647761bd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:5520e3d60a5d01bc8c758c285fe3b2cdcae5b37c34fd1a850a729ecf5e52ceea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233974997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44afccb95b4894cdfb5009863aa75ec674bc7e3bf8d99266034a95deaf62ad0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:19:12 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:19:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:19:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:19:12 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:19:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa275710b614f8717545ff74a69ebe56b1a8c2e299a150d55284d3939a00024c`  
		Last Modified: Wed, 27 May 2026 00:19:29 GMT  
		Size: 165.4 MB (165414684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b51a8498991faee3dac7e001cf5fd3998dee6067bf78610525bdf2d93b4435c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b446a8213b609733c4b71cf7bdd9419fe5e570017d55b5a57d7839ee2472e5`

```dockerfile
```

-	Layers:
	-	`sha256:63bd52e0f6486118c4a3c6cae1353d5239bdd1ff529e619fdf5621a7e7f53e71`  
		Last Modified: Wed, 27 May 2026 00:19:25 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2eca93f442f045bf2e74ab45b72a11bba6230936e98eaf466735cbef76b11591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231866077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839e157bee9d466e842da36d9d83049ca61761521227420312386502c3497885`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:35 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:35 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 27 May 2026 00:18:35 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2109d805bf5a17fc61e16ff3f2c9a3e05114bb5a6433fec33d41a075fc83e771`  
		Last Modified: Wed, 27 May 2026 00:18:53 GMT  
		Size: 164.7 MB (164734343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:59845807f711a8cb14ebe41a64683beffdb09823afa996e7c9e62fa368bf8a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c02fd25e5f2a92651d6323f2c9191096a708a0d39335f6e91b81529d6855cf1`

```dockerfile
```

-	Layers:
	-	`sha256:073a9367a67b2f578dae18ae0372e0bd38ad18d112b4e9eecf61d37edfa13f09`  
		Last Modified: Wed, 27 May 2026 00:18:48 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
