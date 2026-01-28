## `amazoncorretto:11-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:d4e0d34124bea998c5ac2d09fd937f7a8ac798e38756216bb549e15c790c44d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:865dde956c32bba55ce0e5309eb670fc50ce75f1e64126d57cbc7cc197446572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147447698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fca4edc9487d665040f35754f4308eb96fffa20d72f2e960a48d516d0b262de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986d7e858d6100508f42bc906b71c57de3eadb7c1b125079ed3f059f3f83221`  
		Last Modified: Wed, 28 Jan 2026 02:46:38 GMT  
		Size: 143.6 MB (143585877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72034307c503ed790b3266b8c9bfcc0770d7aa0bc7025e40f7c144d4e008f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.6 KB (599611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048f99cc431125d5849132ee52143a8a1e4de02547d103cc78a70b31a0e3de10`

```dockerfile
```

-	Layers:
	-	`sha256:2648d7b5bb643ce264e3aa5cd359e250928ddfb92744b57ed2637fd534055ada`  
		Last Modified: Wed, 28 Jan 2026 02:46:34 GMT  
		Size: 588.9 KB (588929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c50ac0720f14cdc05848940bc58bf3163a47e025123ecbb42d7ff07d51b12f8`  
		Last Modified: Wed, 28 Jan 2026 02:46:34 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d529c0e4180a5d135d8ca8b591b4bf736113794ce198c4f96ed280078716d1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146051586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1040161fa121c96dff3453f474eb5a1f347573847bf908e9952877603c38b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:01 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 18:59:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c016f1d7921cb0297977d531731dee15427272f3b40ad659102fa9e1c718223a`  
		Last Modified: Wed, 21 Jan 2026 18:59:18 GMT  
		Size: 141.9 MB (141855847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9a59e7e8b0b840a947f7483209decf82246d770affb7a11d828638d72bde353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 KB (599217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ab0179a6fc385dda5bad24dbe977b931d7199b9f8afcd7340240f12134c85`

```dockerfile
```

-	Layers:
	-	`sha256:7767a401fe2990247ec6f2327da95c57a971f3a2a152a9d5471239b2a14616ca`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 588.4 KB (588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cae6af08b33660bd64a21076a0352de3c8f68a04f51283e974f7abfd44dc4ba`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
