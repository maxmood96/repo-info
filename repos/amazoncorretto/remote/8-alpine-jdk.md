## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:4af61b0df0ff11f39b4ceb70a037828e050c086184b16b6bfc87a4cd78f46c2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32e5ad0451d37179e0c5ea05fdb34675cb5520bf369d852e617e1d16c917c8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103819027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296840f5588bc26e60d42c9f877a5e633ea94788394b2fdebb8f940870084dfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd673a69bb989e881613aa2f9ca6cf895ac2a03e364198ab3c0a2ce4444c8afc`  
		Last Modified: Tue, 12 Nov 2024 02:12:07 GMT  
		Size: 100.2 MB (100195123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:191dfbe7ee6c8eac2d3e6f6d7384052fc130f4af2915b6d52bf76ccb201349b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 KB (253643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f798417b63c8c8157f47feec1b6b294ed0cce8c423bb0f1d8ff813d10b5fb`

```dockerfile
```

-	Layers:
	-	`sha256:f9549a6291fa58266939436e2604f442cbfc5b60a45ccb1a8a081ad466b799e9`  
		Last Modified: Tue, 12 Nov 2024 02:12:03 GMT  
		Size: 242.9 KB (242948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7188992261675a4407c38642ef70506c481805bb2e5bc449d6312a5d9636bf87`  
		Last Modified: Tue, 12 Nov 2024 02:12:03 GMT  
		Size: 10.7 KB (10695 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:95d92c1ccabeb6e02e6271c9f3c0bf65eef270dd68f5477f9c12302ee6b13e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104066538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc3bca5f49a6d7936d5c7599c33a0c52f467b59b4187267edd13d3828e5d9e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0e098319e117f1f4d0badd0956f33a6df1ba40a57556a74b5b6d5951a713d`  
		Last Modified: Tue, 12 Nov 2024 11:05:28 GMT  
		Size: 100.0 MB (99978812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0db7e1a696754f1fcea40b74971d561e817a250eb515305d74858dbe2fad743a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 KB (253974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a7879ce1616e63f9692ea4f7a576c0362dc2b4ee7fef8ce10721895ae6393e`

```dockerfile
```

-	Layers:
	-	`sha256:416c04686662ebcba05a121b2d3feb1f6d925a18eec81a06845af2aefe5ae01e`  
		Last Modified: Tue, 12 Nov 2024 11:05:26 GMT  
		Size: 243.1 KB (243128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ffe1863fa5d44b37c3843ec7f3a3d2546c65b257665fd1f4ed06aec7afbcd9`  
		Last Modified: Tue, 12 Nov 2024 11:05:26 GMT  
		Size: 10.8 KB (10846 bytes)  
		MIME: application/vnd.in-toto+json
