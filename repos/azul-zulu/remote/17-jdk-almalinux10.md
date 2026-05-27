## `azul-zulu:17-jdk-almalinux10`

```console
$ docker pull azul-zulu@sha256:af869150736890ac422aae9e0f69c22096a1a57ab225845fe6f4f45d2e42777b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-almalinux10` - linux; amd64

```console
$ docker pull azul-zulu@sha256:bf9919a7b5486a2961404166671c60ec92ec0ab1ef14329b7e496d167e745a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220679002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cee192e68dafb389523ec91da77abff838ebf07b9625737408c7f13eb312ca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:12 GMT
ADD almalinux-10-default-amd64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:12 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:54 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:54 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 27 May 2026 00:18:54 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d656c7137a90f7ddb91de182a69468cac7f42400a3d603e1dc41b15db6101bd5`  
		Last Modified: Wed, 27 May 2026 00:13:28 GMT  
		Size: 68.6 MB (68560313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a54fc83a32d3ff895798ac5c74ebdddf6d0468f8ffb1ef776f71d91f89613`  
		Last Modified: Wed, 27 May 2026 00:19:09 GMT  
		Size: 152.1 MB (152118689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:341e61dac9306370bba2aa0306dd82694a3933e2d38638c2777b7588e77391c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455f4ae2600d0ea4d1aa3d5cffb162023b9f040d6683950edc91aa726e5874e8`

```dockerfile
```

-	Layers:
	-	`sha256:d31b9567ba601298a2ae5baaedbd024ef75667743e46855b23300a337330905d`  
		Last Modified: Wed, 27 May 2026 00:19:05 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-almalinux10` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:98c1aaa79401c3cb76c4c4ba586f4e4840f5063b58b307b0f1557613b8b55048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219280212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8be522ef9081b24177bf4dd8058efbad421ec4335727934f9e01519cf0c7ed`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 27 May 2026 00:13:34 GMT
ADD almalinux-10-default-arm64.tar.xz / # buildkit
# Wed, 27 May 2026 00:13:34 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 00:18:22 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 27 May 2026 00:18:22 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2026 00:18:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      dnf install -y --setopt=install_weak_deps=False gnupg2;      curl -fsSL https://repos.azul.com/azul-repo.key -o /tmp/azul-repo.key;      GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;      gpg --batch --import /tmp/azul-repo.key;      gpg --batch --export --armor '27BC0C8CB3D81623F59BDADCB1998361219BD9C9' > /etc/pki/rpm-gpg/RPM-GPG-KEY-azul;      gpgconf --kill all; rm -rf "$GNUPGHOME";      rm /tmp/azul-repo.key;      printf '%s\n'        '[zulu-openjdk]'        'name=zulu-openjdk - Azul Systems Inc., Zulu packages'        "baseurl=https://$REPO_HOST/zulu/rpm"        'enabled=1'        'gpgcheck=1'        'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-azul'        > /etc/yum.repos.d/zulu-openjdk.repo;      dnf install -y --setopt=install_weak_deps=False fontconfig        zulu17-jdk-17.0.19-3;      dnf remove -y gnupg2;      dnf clean all; rm -rf /var/cache/dnf;      java -version # buildkit
# Wed, 27 May 2026 00:18:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 27 May 2026 00:18:22 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:18:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2e6581d4e57d2c64e98e26766f719408796b49ab923bb5ba71515cd98debeafe`  
		Last Modified: Wed, 27 May 2026 00:13:50 GMT  
		Size: 67.1 MB (67131734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a8fe7501a08b08d7a09fcb95edbd80ee0fe34cd6cc972dd848a9cfcaa07ba1`  
		Last Modified: Wed, 27 May 2026 00:18:39 GMT  
		Size: 152.1 MB (152148478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-almalinux10` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:907e663e0b6bbc6b762c2adaa3406f06df47812fc0a6d3311c9e432ae6a01772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4413ee2e32e3e0ec1d900490e376c98b36bf64c93c483204f40f6aad5b7aa928`

```dockerfile
```

-	Layers:
	-	`sha256:7c3308eeeadcdee68e5ab88b8dbbd8a82dcdaa89c6508b550a41fc93695be567`  
		Last Modified: Wed, 27 May 2026 00:18:35 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
