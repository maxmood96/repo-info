## `amazoncorretto:17-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:ac45489ce3ac30e9758d3354a60c63a2e962d102e62dd1a1ef816ad6aad58fdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b7663475359f6fdc8cbe26fadb9c30a5e43055152deb1ec5be352a7369ee8d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149437707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2235a598064e1e9cd8c7497b909abecd3b387569158b3e21d70237cfd3408ded`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e00752353d83bf5bef20f54db7fb2bebaea79e596bb880c1f8da111667d6bb5`  
		Last Modified: Fri, 06 Sep 2024 23:17:29 GMT  
		Size: 146.0 MB (146018001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14882e1754e51d1e6b1520f2676e5b949e469b87d22cf75bd8ae87ee361a5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 KB (389935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54642bcba4c394c576aec204a2f08abd9ed65eb9b53bca2a4d2a49aae4675e4`

```dockerfile
```

-	Layers:
	-	`sha256:ff7be1dbaf8873786f695110550c9709d30716cfdd0260b4bf167539c0aea13a`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 380.8 KB (380763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9c524b4633e36913fe5589eced74ea0ed3cdb51648c8f356f3c58b76209051`  
		Last Modified: Fri, 06 Sep 2024 23:17:26 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d7f3dcb8dece2aada356083dd35c1d2f99da1643dca205b557247d6875a5b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147709989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd7318a74b3812f93b2d59a77145ce91c58282121703d1693f22413e68c86ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4a2927f89af212cd4c69c412603f01e795a72ebbdc2ade8af5e61e3b141a8e`  
		Last Modified: Sat, 07 Sep 2024 12:12:21 GMT  
		Size: 144.4 MB (144350886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:59bacca397156e133b44781ad451644d0c12eb622b8e1f64c64742b5e6537580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710c4f0db349b002714fe530c26a64c3f8edccc28ace9047f7fa08c18f72959f`

```dockerfile
```

-	Layers:
	-	`sha256:19d6cccd22a662caeebe56e75c8fb7f4075f72c6094824b5cf03bddbefcb931f`  
		Last Modified: Sat, 07 Sep 2024 12:12:18 GMT  
		Size: 380.2 KB (380181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28531b2acdc112af67963d3d43f941856642ccff89a2c8aeb615d74a3f796850`  
		Last Modified: Sat, 07 Sep 2024 12:12:18 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
