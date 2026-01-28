## `amazoncorretto:25-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:77031d1515503a994b65f3ecde4b402d0e0cc7ef8fdaa573a79e1075a7f64fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:087b0c44c7b7376bf1cc2d3688bbc1f03c3716ae276aa972b2733658bbb870f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184379016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61e00639e690ca4f6b5f7d5fb11925b42db1b7241bb550d646470a0024aadfa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:50:57 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:50:57 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:50:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:50:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:50:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307d6170e04765e491324329a6097cc32161772d7bb12602a8a131b29b740948`  
		Last Modified: Wed, 28 Jan 2026 02:51:17 GMT  
		Size: 180.8 MB (180751152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:631ec6952f29fa0fde3e454757b2b5d0b9fefda1d241b3cec63b0e46c2d0fd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 KB (599026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b61083d683b3ec1d34d09a8ac9653068d4bfbe580a074d4891b0921165c61b`

```dockerfile
```

-	Layers:
	-	`sha256:13f25dcf239198bb1d9709b8e56b2a91392382d97905a3662f2e7c1bb04d1a7f`  
		Last Modified: Wed, 28 Jan 2026 02:51:13 GMT  
		Size: 589.7 KB (589655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c67094018f208172a0870ddd992aa7b136c12cc5e66ff7c3850e5d7154c7b2`  
		Last Modified: Wed, 28 Jan 2026 02:51:13 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5d86c7e9ffc9f7eb0c7fff8a45b7d2cbad8028e855c749a745a6c539d0f91478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182505717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d928b5f9a97671711f4d75c88e94129330f28b22db1e3bb01bf427d9d306b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:53 GMT
ARG version=25.0.2.10.1
# Wed, 21 Jan 2026 19:01:53 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2589f56c81038d457005af3c5765c0e3f672f5254014f755e027d0188590811c`  
		Last Modified: Wed, 21 Jan 2026 19:02:15 GMT  
		Size: 178.4 MB (178416340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e22152673020aa12ae7dc91e0d01a90ffa26ca0853822f126fb376c4cc51746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca47716baeca092bd0c605378b6d91694260e363b9eb9d0209385da104e97a58`

```dockerfile
```

-	Layers:
	-	`sha256:0a307cb75896ec3767ff8c7a27946946ab6779de5bbf29f2523ed824f4f0f4ee`  
		Last Modified: Wed, 21 Jan 2026 19:02:11 GMT  
		Size: 589.1 KB (589071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13212626b579c622b9b31cb54106217959f5dffc15de85fbe513c9737899db94`  
		Last Modified: Wed, 21 Jan 2026 19:02:11 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
