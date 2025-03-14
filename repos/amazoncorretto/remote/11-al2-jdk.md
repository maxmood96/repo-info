## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:89b6c49b62d84d7a8f769e43ab03f0fb016dbf90cd768629b9d9b6efe9be6940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4d452e3ba851e930202b2bbb9e8d5f072e289bdd46bfacc28b73a3d81fff50d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211030923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866132b767c428e99ca22706eaec6221f2e3759636c8d34106f66626a455cca6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548edc7be46df240871aa3e0594d1b13a0738d3ee4fb417da69775e243d3c79`  
		Last Modified: Thu, 13 Mar 2025 23:09:36 GMT  
		Size: 148.3 MB (148258085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd58dfbb1e28451e47b9b2cfc14df9213af37740b4d13143a3e23a6a45058a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee7dc7a2ab21a7669486e4ac8bcaff9b2759944eb4e2c1377e2f97f37cfd9d`

```dockerfile
```

-	Layers:
	-	`sha256:b111a9d7be70f6ae04752eb7d5da32a56ed9404de119953c71be00da0e5a2e8f`  
		Last Modified: Thu, 13 Mar 2025 23:09:34 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3eceb10446f4f98ec22f6245f510f4287f60c39eec9ddc9ed3db1c3fd2c3d1`  
		Last Modified: Thu, 13 Mar 2025 23:09:34 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f14547b14986fb8c6b46047dba2c97e62146bdf08fa728e778d1d4e6aab0c89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209884942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a24add8038cb68e9035bf5f47085f397bcbf12ce34c200334fd809d160c3228`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d83fe85e2c73baeb609660ba452051dc9b4cd5d05b81dc306beea0a1fd531f`  
		Last Modified: Fri, 14 Mar 2025 02:25:46 GMT  
		Size: 145.3 MB (145308088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da098ebaeafeed53020eb13f5108e10847f34cf0f249c17254f6112ab95f5d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e84fa23b723b23e2010ade5165d75a7aa716d0bcc797aabf77e8dbb3dc4570b`

```dockerfile
```

-	Layers:
	-	`sha256:1f2679d4cd37e6350321a32e8bb8dfa5953529af771f34a6a6d716ff22a11fa4`  
		Last Modified: Fri, 14 Mar 2025 02:25:43 GMT  
		Size: 5.5 MB (5523909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12bb1cb1588db1b42eaa268aa1b069102eb03ba08931036d6a909a8d8977b5b5`  
		Last Modified: Fri, 14 Mar 2025 02:25:42 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
