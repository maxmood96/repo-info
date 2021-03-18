## `amazoncorretto:16-al2-full`

```console
$ docker pull amazoncorretto@sha256:fba1f65d4c482aabdc953f07a7cc71e5eaf29ee27989836dc00d369c098957d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:049000605566e78edc28620584d15be53d6a52a4523b9127959590ab9bf03f9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221870649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574534f6ee837df7df893438e0813be532c93273c3cc96d874b09e37b7cd8e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Feb 2021 19:19:48 GMT
ADD file:40bc6ac9b95149d9077e8e692feea2208fcd1c5883673953b295e6acd014ea38 in / 
# Wed, 24 Feb 2021 19:19:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 01:21:21 GMT
ARG version=16.0.0.36-1
# Thu, 18 Mar 2021 01:21:37 GMT
# ARGS: version=16.0.0.36-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 18 Mar 2021 01:21:38 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:21:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:9da98c321efd693e1dc19cc24c7c2cfa365c649f178da8ebdfdc5243d0b2f91a`  
		Last Modified: Wed, 24 Feb 2021 10:37:31 GMT  
		Size: 61.9 MB (61935160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9092c7df833910471d3e8ee541a2f28a3659972660474f01a9fab4e6ae8f56`  
		Last Modified: Thu, 18 Mar 2021 01:26:31 GMT  
		Size: 159.9 MB (159935489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f126d71e74c4b61b4b8cf4dc4f9dd5a1375fc1dda1ff281ddd63b6a1d9a9f34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223515735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2dec0095bd7699386451e858d5eb8062256c862bf1702753d05553bf6f191`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 24 Feb 2021 18:44:28 GMT
ADD file:e57e27bb2d338405f702e133eb22bfd61d172471ce8bad647c7f7d9b0b30bf7b in / 
# Wed, 24 Feb 2021 18:44:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Mar 2021 00:39:54 GMT
ARG version=16.0.0.36-1
# Thu, 18 Mar 2021 00:40:33 GMT
# ARGS: version=16.0.0.36-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 18 Mar 2021 00:40:35 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 00:40:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:c669744e929468ab3571a83e2386710816116036b648ebd90ecc44d86705b51e`  
		Last Modified: Wed, 24 Feb 2021 18:45:40 GMT  
		Size: 63.6 MB (63624537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2214528904f7c29ecf0ff8106a2ca25b33ec6dbc5e51ff3e0e8cc46c35d3d97c`  
		Last Modified: Thu, 18 Mar 2021 00:41:35 GMT  
		Size: 159.9 MB (159891198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
