## `amazoncorretto:17-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:5d181cac3374a7c065a275aed25ccb554e764df84d7c457e402bbe5082578ef3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f4b653770136e0d7292e59a19c21d20211458a316a9334f5915b1b5a9bdffb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151963507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bbe93e52f1662fe9df4404effa3c7e83a781b93efe043b68ec1114c307c4d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc638603b06e6d2629cc5b42fe600f9ded4be316be1868d76c0759576dff74`  
		Last Modified: Tue, 21 Oct 2025 23:27:40 GMT  
		Size: 148.3 MB (148336451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5ef83d43fefc5d81a734b30c0e946589980eb839730af2571ae6d42d1745b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.1 KB (590078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9099ced3e5e8b232f65757496a84b76c74d3f21a2ae3a717c63d56e4b222e9ea`

```dockerfile
```

-	Layers:
	-	`sha256:5a0b2ac3d5c79bed836e613558abf663f43b3439e6798480e69ecfa983240ab7`  
		Last Modified: Tue, 21 Oct 2025 23:27:37 GMT  
		Size: 580.7 KB (580656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cdad30046fed778d5aa7a8fa084f352d83a2c000aa3abd8a28a3ac862ddf11`  
		Last Modified: Sun, 21 Dec 2025 04:53:48 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6d8c3419d40f894db0b5ebf677320ebe549f08f6c411eb4ab8c4999447ac07ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150803944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0125f93581f17d4a7c320db377e96cd8ebc3489d3de373a7202a306b405b06a0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fc065f1384bc167050d7b8ba6683eea22c93bbe8bf5be6a53fe9765ae60b92`  
		Last Modified: Sun, 21 Dec 2025 06:59:52 GMT  
		Size: 146.7 MB (146714567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24e139427e522999c98fedd41fc657ca47d1f5996a320ae99574c36881838471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.6 KB (589601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2e5fbbbd3117136b3c290937f70608c2867df122bb887ffaf2e7165b44e1fd`

```dockerfile
```

-	Layers:
	-	`sha256:f782ce64d1ecd70f8d3683b9c6399a002074eed314da0127e4f1c4290a2043e3`  
		Last Modified: Tue, 21 Oct 2025 21:50:21 GMT  
		Size: 580.1 KB (580075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4568f807d460d1b72dcff11755dd1b386b499f45ca03c3fd42e5850aef93aaa0`  
		Last Modified: Tue, 21 Oct 2025 21:50:21 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
