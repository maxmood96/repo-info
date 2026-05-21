## `azul-zulu:25-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:7be8c5a61eed375de5da6732f7cceb2196d9a60d19dc7063f6e7d1b8a06b46ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b08ce2ea5c79e6613a40209883e3d12f36f813d9894186890ba76b1dde37a3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252316837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7b871d5256791af3859a92a5f6a24a1b1c0858a9f9a7c0e2374604176cafc4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:16:02 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:16:02 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:16:02 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:16:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 20 May 2026 21:16:02 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108911c08336ff0113b35566a3ff5a90d03f6bf5b21c92617d27aa7800db6a95`  
		Last Modified: Wed, 20 May 2026 21:16:20 GMT  
		Size: 183.9 MB (183860235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1839f522e6f9bfd238f1a0ca4621846ab25c6ce89b6d99a50db1d3b370ccc283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce195b0cf5e40b2dbcabb138de40a95c2f85de95ced2bef06eec1b98cbc46037`

```dockerfile
```

-	Layers:
	-	`sha256:54c76293139124713c670258619818b1c9e096452ed67b1aa85bdc5ffff3d0a5`  
		Last Modified: Wed, 20 May 2026 21:16:16 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:db4eb659b6843d9c082608d4422bd1ab12e0c8ee91c38dcb07d3c4bc28ab7daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249979674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0815339df91c2e8d6e20eb0dcf45b34da307e43ebba0274bd305046bb32cb3d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:32 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jdk-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 20 May 2026 21:28:32 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:28:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7990f75f7dfb0341fe34c503b6336d89a085d7a68862e1d29b61f03156f6f2`  
		Last Modified: Wed, 20 May 2026 21:28:52 GMT  
		Size: 183.0 MB (183009505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d297a35bbee1a9f5b4da28c666233d76a42d033bbc1b3d8722a390a710b3109f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b433776816beb123e53dbc39ed7e93d9161a79d11d3cb29dcc8af38d67a338`

```dockerfile
```

-	Layers:
	-	`sha256:da78f9041e6ae8dfffb3458c501be1ebd3157fa55572cf617ac50ebee1f4bed7`  
		Last Modified: Wed, 20 May 2026 21:28:48 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
