## `amazoncorretto:20-al2-full`

```console
$ docker pull amazoncorretto@sha256:ffc85f9d43f43cc9bbded389d74473972850bd89914bcc2ec0568373b8086191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c4c5d1bfe544f415faa2d3e3136b16fc23cab0e3bcb843f934a597540a27aee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223252795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb1b5b014f6eccc33f67925b74dad9887300ba8234f40062b95b8ae370dcf4a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 01:20:13 GMT
COPY dir:be29c71398840090bec7021ae8f2d354451564507602cf38257ad90a915b1838 in / 
# Thu, 13 Jul 2023 01:20:13 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:46:54 GMT
ARG version=20.0.1.9-1
# Thu, 13 Jul 2023 01:47:18 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 13 Jul 2023 01:47:18 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:47:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:e90aa42bc48ff728ab10fd485b42144e863dfd8689dd6ea94c78ac0357ec5101`  
		Last Modified: Fri, 30 Jun 2023 00:09:38 GMT  
		Size: 62.5 MB (62485766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef031c6bf01ba287ce407eb5d14ae9d9665c43c87e362added9b16891e682ef2`  
		Last Modified: Thu, 13 Jul 2023 01:55:57 GMT  
		Size: 160.8 MB (160767029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a0ae8ac481fcfe3a770ac183b3887ffe373abad9aa7d2874dd77b1702d56bff6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222928362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7abc320b0fe7107c99e3e5b41c37f909337ac9c07e99eb664b9c8b3eb938535d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 00:40:00 GMT
COPY dir:a284fdf4a484ebc9131c665fc151094ec73265d07d353476272944e301722064 in / 
# Thu, 13 Jul 2023 00:40:01 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:11:08 GMT
ARG version=20.0.1.9-1
# Thu, 13 Jul 2023 01:11:27 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 13 Jul 2023 01:11:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:20c8bca6ae5daad56b485a4b6f1f395a51727d69eb6a7566c53b00a366e46576`  
		Last Modified: Fri, 30 Jun 2023 17:38:06 GMT  
		Size: 64.1 MB (64128925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2fe269925b1fc2448bd27586fd47ded5d1d6a0ab53705a653dbe68cde80b7b`  
		Last Modified: Thu, 13 Jul 2023 01:18:38 GMT  
		Size: 158.8 MB (158799437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
