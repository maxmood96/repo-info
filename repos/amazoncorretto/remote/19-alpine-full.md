## `amazoncorretto:19-alpine-full`

```console
$ docker pull amazoncorretto@sha256:04680e785628895f65473f9d51b7b4f05fbf7b0c453b90c3c6fc9d04addce9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:545931863ab3541ff755312355bb90c9d823530d5edc53ea7b2760262011cdb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203021619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d0c67c72f16a72199c2c70a9f8173e4a70f705fcf976bdb2c071438e217d3c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:21:09 GMT
ARG version=19.0.0.36.1
# Wed, 28 Sep 2022 21:21:15 GMT
# ARGS: version=19.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Wed, 28 Sep 2022 21:21:16 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:21:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Sep 2022 21:21:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b8617849b9105cc50b5fb6ac8ef04dfa256d526db15faddda8f4d4588edd1e`  
		Last Modified: Wed, 28 Sep 2022 21:27:00 GMT  
		Size: 200.2 MB (200215565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
