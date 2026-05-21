## `azul-zulu:17-almalinux10`

```console
$ docker pull azul-zulu@sha256:d9dc448783dbe4c4a52116c9f5276fc985938f0ca16ee9fdacc1c4f94331f325
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:0e3bb158d44e30f75fce357e0a0192fcb2f8f6beb3a052905eb7b2427cfa10a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220626868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b7072e9adda145c8dff43372d7de0e39df385b62bf223b78cf8a2d29859726`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:31 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:31 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:31 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 20 May 2026 21:15:31 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:15:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac91737f49869f184684aae810af9bcfc960547afd947c2e65d2aa843d39e27`  
		Last Modified: Wed, 20 May 2026 21:15:47 GMT  
		Size: 152.2 MB (152170266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:081d8e3057d6d34be6bac421e7f693c024e34bd3c2f8d212edb6abca41eec501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a94734dc0b856b31ed6b9f04a2484a82150a9f45aa04930bed849835314ed8`

```dockerfile
```

-	Layers:
	-	`sha256:8ce9f9b10aded27f54e16f0be78bfb9718047a6973d729a3c01004be437d426d`  
		Last Modified: Wed, 20 May 2026 21:15:43 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:89e821bb926cb5ff602e9abdbd1dc7b4977c644da22714db7ca5d4c2af851ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219168714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0850aff780ac6d8e501f27a49c3776b4d2e1d7268dd8958f9a84a960defd5d06`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:27:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:27:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:27:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:27:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 20 May 2026 21:27:32 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:27:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06dec367e4d0ebd9a9f66f577e7470182495b33413985f96df5c7b68754f0ea`  
		Last Modified: Wed, 20 May 2026 21:27:49 GMT  
		Size: 152.2 MB (152198545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ec551298fc7a1e1cc8cc961295ca39190cb7ce382b2732891306194a95e29591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8004bae9a973bae3eb8454428697560448b5471d913f7c9902ae9b2a8f10a639`

```dockerfile
```

-	Layers:
	-	`sha256:d22d60a93da0248bd04f381eaf96c297c8b744e581cd78cb875e16da87f24609`  
		Last Modified: Wed, 20 May 2026 21:27:45 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json
