## `azul-zulu:21-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:acbaf94592fe6f6760cffb80f990e55031a34ffddeea90ac662061e75b6f7a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:79d4047b76c889423bd41c26ccaf245e95c12fd00ba08c1e7a54a4648387db70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233246983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504287022dd0cac214466b7b77d96432a6692dd38d1881e26b589c703f092e2c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:22 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:22 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:15:25 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:15:25 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:15:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:15:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:15:25 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:15:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ca4bc012c6270dd0dab29783ab29d65b691d6b8f3ca1a92c5a8bfe9d51019a`  
		Last Modified: Mon, 11 May 2026 16:40:39 GMT  
		Size: 68.5 MB (68456602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada0356c4f9a8c53cbca954203df2306e929b8c96ea5dc513ec22abde68fa0ba`  
		Last Modified: Wed, 20 May 2026 21:15:41 GMT  
		Size: 164.8 MB (164790381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bfe6a8c788aff939dd0ad440ae1810a0a29be6d8d304985c5eb182d7854e30db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f03cd6db6279769ca77d20e63c969749bc892bfc3a2d9401dbb21ec4c37f449`

```dockerfile
```

-	Layers:
	-	`sha256:670a7e3ba2c0418f69c2ef57574d8594b4f4dcf8cba858671e70e1f9cfa971ac`  
		Last Modified: Wed, 20 May 2026 21:15:37 GMT  
		Size: 9.2 KB (9239 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:95114411a6d326e7198abdfb4cc841ef1433b04b2b105d7e5dc68c1486986965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231061650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5159da712bf69e93ed4152e11e46e60d7e37d75a1fc245a22eaad6919075e3e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 16:40:15 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Mon, 11 May 2026 16:40:15 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 21:28:22 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 20 May 2026 21:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 21:28:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jdk-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 20 May 2026 21:28:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 20 May 2026 21:28:22 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 21:28:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:130dad5a52e276fdeb93dfac0bfa9126abc7121797fc1d218ebf01cf7201f1f0`  
		Last Modified: Mon, 11 May 2026 16:40:33 GMT  
		Size: 67.0 MB (66970169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f686e781754a83b72199aca03331c1b091ce15dc5f2cb2a51f1d3aa2551b927`  
		Last Modified: Wed, 20 May 2026 21:28:41 GMT  
		Size: 164.1 MB (164091481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d63d366511bd98fec3faaf46b7c722a22c2faa7db36278f42d70bbf87c1858fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc4a91f78bcf3270900168d121b1ebc9ce5ec6071aaac8213ff9a7711584ef1`

```dockerfile
```

-	Layers:
	-	`sha256:81d758847d12a9380cd798cd9d83f6bc194f38c3c1294d182be956ae0ae73c76`  
		Last Modified: Wed, 20 May 2026 21:28:36 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json
