## `amazoncorretto:22-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:53742d68fdda3dbbaf78ce435e62947a9fb70157ebeed673902f303cb153728b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a3f2682dbc89d08930ff00041fcbe4728f70c1571dd7ceb3edb817ab795ec72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161015937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efea864465c5379330b7184ef97a97432016227cec1b91e80f1dc7dc20e551a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:20b21bae5545b74a497ba0793872e6960b3e12d9bc20fb67ed95f64851079651`  
		Last Modified: Fri, 06 Sep 2024 23:18:04 GMT  
		Size: 157.6 MB (157596231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f9ff3064948bb1942cfe5f618f9904fe6a8e8eb72af8a919a5ba7e118e52a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 KB (391075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fc95ae81fa770e2c47c1d91ac2a7eedc59b131eee085698190079128edd740`

```dockerfile
```

-	Layers:
	-	`sha256:f22b0916c2e73df94ee0e557d08614e8f0bf9ab501a0d36b22e507ad8e7e7000`  
		Last Modified: Fri, 06 Sep 2024 23:18:00 GMT  
		Size: 381.9 KB (381906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc08216cb0c532f9deff68d41b459961dccbafba265840488a3a56bb3299a3e7`  
		Last Modified: Fri, 06 Sep 2024 23:18:00 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a31ee6183fe5731f75d9555d2101270f77dda646a048cfc219647451c171196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158553790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d5bfa1e2bfece7bc37b47a17a8d7e93e6fa8d68d60bebc935f9f912ee85236`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:b13b9488474936147aa54f75b532f584bddb11669b9680db9565686b22f6296b`  
		Last Modified: Sat, 07 Sep 2024 12:17:26 GMT  
		Size: 155.2 MB (155194687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9907b5c3e6c2b52ed2312f1fa25d221667e6640efa160e9cb2a05961cd51763a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9ae20247ec2cf25d91bddb1eb8c028cbd8536ad13c6c5b8769f99d6497b05e`

```dockerfile
```

-	Layers:
	-	`sha256:c8509868f3a0cc65fe6ecb8b5f84baf3ededec9e9ea6def270c3dd635074bb6c`  
		Last Modified: Sat, 07 Sep 2024 12:17:23 GMT  
		Size: 380.7 KB (380683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da5ffbf7ea6c87b50816465af80b48fc6f62b1cdb9c5ff20b8e5a885f0226c7`  
		Last Modified: Sat, 07 Sep 2024 12:17:22 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
