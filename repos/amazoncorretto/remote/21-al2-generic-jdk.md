## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:b69f66a15ed0eb88fc67bbe9f3b42d9683eb15d2093b52fa3f9b54ac41e8a5f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb0582ecfcdc1da2b2b5eb0c1597025c00dcb6d17b54acc59798d111ea331cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228482102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988becc40c2aee3b465b7770fd5f029cb79a8df393e1d66761cb1fae10b3ffc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8209275f923a180dd87535f2386dd1dcb42c2f09ef561188033424bc5857feae`  
		Last Modified: Tue, 24 Sep 2024 01:57:59 GMT  
		Size: 165.8 MB (165803568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b95bb909eca04c2f1826b9fd7c4e2ac5f5aa44b3841a68c49e59e47699313a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 KB (10995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87628ceb87b28b1cef8049cfdbf28a6ccfa837fe3a9831876252854ba8398ae`

```dockerfile
```

-	Layers:
	-	`sha256:89a5804cf181edd88a0f9e14ddf6e50c0968f47fab2d34b4690454b8f56af292`  
		Last Modified: Tue, 24 Sep 2024 01:57:55 GMT  
		Size: 11.0 KB (10995 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d42f71a1bded2cc5f9ab0c866cbe94c3684dcb013c366120d2a0fa60da0fdc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228406930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7547ea6397f82660a11881a4953e6cb0fef57047a5182811116c662dd0dfaf95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d21619c9feeafe24fc45c11645e23e593781a0a9acf5090729190d13af4a2b9`  
		Last Modified: Tue, 24 Sep 2024 02:42:43 GMT  
		Size: 163.8 MB (163820383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e9e97abee2e5516e88c870c1efe03d2202971386b568590b5952f5ee612d7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350fc7579abfc522645274ef9f80ed72e360955de8e068a62bef0a7f6f321586`

```dockerfile
```

-	Layers:
	-	`sha256:f0b8258d8aa5effed24772fcb7f7555a8d352855d156332392b84394fd69b20e`  
		Last Modified: Tue, 24 Sep 2024 02:42:38 GMT  
		Size: 5.5 MB (5526353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3f3148c810690fa989bce5ce50a08bad4b991f3c36649d6d50e412529d17fe`  
		Last Modified: Tue, 24 Sep 2024 02:42:37 GMT  
		Size: 11.6 KB (11647 bytes)  
		MIME: application/vnd.in-toto+json
