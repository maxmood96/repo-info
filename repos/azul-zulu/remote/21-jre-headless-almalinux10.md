## `azul-zulu:21-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:b31920307f2ba62b6345e9db467da8b50a90f3115ac93688694d7fb1a729ace8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:92eeb2d612536ca0bede4db5cc6bbdfed63e334f37fc724df20ff0a5715df882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144289480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cafcfcd9b9f5ebfcb56be5ccd3c22d910504dcf37c52844f22b0d1261826749`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:09 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:09 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:09 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffba6134f1b583cd9436ba5615244edf125cd9e595a1a3b01949345f4d6477`  
		Last Modified: Tue, 02 Jun 2026 19:08:21 GMT  
		Size: 75.7 MB (75727018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b6e856616f282297db766e2e9a5b1d3ef50608c3b083c6d1dd76e7f665cdf775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914fe5148facafc51a4fd96b4e57971eb80ef2bdd801efd79db932114231e429`

```dockerfile
```

-	Layers:
	-	`sha256:40994699fd6582f5b094edf5334767db27f96ca8ac38cd9a34ee02003238942d`  
		Last Modified: Tue, 02 Jun 2026 19:08:18 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ec918c80b92f5f68e0204c38cdd374d87906f53260f6428190c199af3420c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142517132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de3741f1d278641c463ca318ad1fbc1aa06692d5c90ba8887f634acdb21d676`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:31 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:31 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:31 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu21-jre-headless-21.0.11-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 02 Jun 2026 19:08:31 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123acebeeedbe08f8ab15bb9dd654b96f6b21e4240a98d79cc5597efd78c0629`  
		Last Modified: Tue, 02 Jun 2026 19:08:44 GMT  
		Size: 75.4 MB (75375171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:96a11911b60206772f7a372a276197c98e412696a2d8c9196e9436751cc262dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893267acba3a90560c53db522a8cb31573065b9a67dbc15aeb69d1bb2e051961`

```dockerfile
```

-	Layers:
	-	`sha256:2bddce98115a49db3844d91bb6350ecddcd1049a758521782fce07c6d6f9d190`  
		Last Modified: Tue, 02 Jun 2026 19:08:41 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json
