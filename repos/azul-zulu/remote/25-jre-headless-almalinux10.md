## `azul-zulu:25-jre-headless-almalinux10`

```console
$ docker pull azul-zulu@sha256:23eb64f2706fabb3348058d2fb6cd62ae5e83ae29ca27d59217bcae85d1fc32a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:58b1007de493076d0a753bfc76effa6b3fb9e67647256e9fad5ba1e76a7f479f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158441788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d4dca9f4e3377eab54ccdce7c6f8082a495c6864a474c42f4caa6027be83f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:16 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:28 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:28 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:28 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:28 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:4224950577242fb7ff1faf31d7a6c1520d455ab1a1eecff8aed5766688091539`  
		Last Modified: Tue, 02 Jun 2026 19:04:32 GMT  
		Size: 68.6 MB (68562462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5522013d6f951317d69117563150d6b5d72307d04d9d04dba85d14f16c5df5`  
		Last Modified: Tue, 02 Jun 2026 19:08:42 GMT  
		Size: 89.9 MB (89879326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d1a88bf8e739618dcb684278e42a534912263a9cb4ced816b3b9f990ec33fa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00341dad400ca371d06113a6c25350165d1de3309ba94d885afe4f3ac81cda93`

```dockerfile
```

-	Layers:
	-	`sha256:8a2ff0dc822fdd512b5347645180572ffb2f0af32b89b62fa98eeda5d4ed793f`  
		Last Modified: Tue, 02 Jun 2026 19:08:40 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a878c2a93cb5e2ecc7507fc3952379ce2ea480529e760a03182926efc57ea2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156630143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd17b529bdfd8a7fa3937550f496d509d7a730d5ae0c48449dfefa7e0038f705`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 02 Jun 2026 19:04:37 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Tue, 02 Jun 2026 19:04:37 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 19:08:49 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 02 Jun 2026 19:08:49 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 19:08:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu25-jre-headless-25.0.3-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Tue, 02 Jun 2026 19:08:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 02 Jun 2026 19:08:49 GMT
ENV PATH=/usr/lib/jvm/zulu25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:11aaeaf9729fbc9690ea62f609dd17fc5d9fca4e16048f27425d411f758066b2`  
		Last Modified: Tue, 02 Jun 2026 19:04:54 GMT  
		Size: 67.1 MB (67141961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c94412d1c0a9853dc875caefc5bbed1022b43b0600f0760124deeadc11e5c`  
		Last Modified: Tue, 02 Jun 2026 19:09:04 GMT  
		Size: 89.5 MB (89488182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:aba6a883001765e9a32776f3474afab740f0970803f3f19bb15b66aba4dd6b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2047ba5ee63309339f35276618ef18a790cc1884e85cf541c41aec23ffa21c7`

```dockerfile
```

-	Layers:
	-	`sha256:d14d64dfbea5a6ddced3d24b5b0afbb6ac8af1c7dac90cacede784dace733f2f`  
		Last Modified: Tue, 02 Jun 2026 19:09:02 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json
