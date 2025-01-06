## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:8b16834e7fabfc62d4c8faa22de5df97f99627f148058d52718054aaa4ea3674
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f3e9cef8e99e55bae620641a79fd4cdf361c6911862c0fa304072d88e6739472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162554041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6876e84cb6b1455a4b0963623b037af045271f321104d2e067f1799ba48fc963`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:7cf047165709bffe3a3624e99cceb7a7bf696113e52c26ecebfa07a01fc0ac18`  
		Last Modified: Tue, 12 Nov 2024 02:12:35 GMT  
		Size: 158.9 MB (158930137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:083d35fb866df23d93435ec1a4f5faa49a3e82d10453fedc8c697b1ebbf2c0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b9d22bcf0c885ad05a787e9beacd46d1b9e8170fcc93670b3f9ce99aa331f`

```dockerfile
```

-	Layers:
	-	`sha256:77f33bbb6f8ab0f0f4cb092e8fc9e0c2b1903c578d0220d178f7757012fe825f`  
		Last Modified: Tue, 12 Nov 2024 02:12:33 GMT  
		Size: 378.5 KB (378492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a499727f0d67590d784b2d513234d79ca2d194c746255654f24fa6d6be0b4ee6`  
		Last Modified: Tue, 12 Nov 2024 02:12:33 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a1baff800c62ca66638aa50c2a42aeddc1a8ed856265716052990950eb64e286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160967815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00943b443b37e79b13b6e8fd4111f5d5e2b7859721764b201ab1b1a7e405e0f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:204f41bc5b0b52b89a1e69dff490ba86e013e780b9832889254fe40822df6abd`  
		Size: 156.9 MB (156880089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2b25adbd8670a8286171921e34fe87ec1f80e0cd37ed4b5774fcb362159e8cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 KB (388831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f5b3caff542a755f939642a8058418c30fda93e2cedf4960e3cb60acc8adbf`

```dockerfile
```

-	Layers:
	-	`sha256:c81dd4c126c80d3c20a92a5b509fb4a0507a0c273215b7ce1c19efb8b8eb9000`  
		Size: 378.0 KB (377958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82ce3967d37c4c505314f8e993c41ed84111487e40b0bdd81c5b50ad1089dc3`  
		Last Modified: Tue, 12 Nov 2024 11:12:45 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
