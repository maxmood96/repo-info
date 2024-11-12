## `amazoncorretto:21-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:038240b42693a3d8f5f5a1820205e1d151e33223b957a7d99709db2d35135a09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eacc10477e9a7f76be5fbcb2369ae69bfb0b5e5ded5405025632c3d58f2ab8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162321737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ff34931bc2b197a6ca0be548d8cc3eafc13861547bc6412cc292a7a8686b8c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:02:06 GMT
ADD alpine-minirootfs-3.17.10-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:02:06 GMT
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
	-	`sha256:fbcfea79c1c4819e0689385057cfd4cbd2ee9ba20e6d420b360644788a22862c`  
		Last Modified: Mon, 09 Sep 2024 07:01:59 GMT  
		Size: 3.4 MB (3392252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbddc550d1bc979dc6510515fd7d1dd1aafedc9f168f9b6b34d4022b55824571`  
		Last Modified: Tue, 12 Nov 2024 02:12:26 GMT  
		Size: 158.9 MB (158929485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8685afb02e2ffef310dc94b3ec070ddac89697389a3a587da0b0844409620504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.6 KB (389574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59440c77b1147e1ad9668fda4174ef9de09acd73d478cf1cdff884b92fa816b4`

```dockerfile
```

-	Layers:
	-	`sha256:1aaabfe57788d53b61243e0cdc80480d45391e904eb0071b367a8fb961f9e57f`  
		Last Modified: Tue, 12 Nov 2024 02:12:24 GMT  
		Size: 380.2 KB (380159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b32116124ca3a300bb94728db2ebfa2e278aa4d4a181b62b4b215a46b46d7e`  
		Last Modified: Tue, 12 Nov 2024 02:12:24 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:901fa5c59e5a733de308bd4e3fa2e1ca39f28570277c431ce04b2b42214e1aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160153525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1497f8cd83ee2ca7bf5cff3c54c993f509b6d3405548932c98ea32b550261`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:24 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Fri, 06 Sep 2024 22:44:24 GMT
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
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae142aa96cc6b8db3fb7ccf5cd417003dba5c5b2e258bc268514ed84c1b9eaa9`  
		Last Modified: Wed, 16 Oct 2024 18:36:29 GMT  
		Size: 156.9 MB (156878453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaac0fda31a00e8ad6fc070bbc879b42c5a5010a13d14784991b752f6c2cfe16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 KB (388790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12894a1ad92f0ebab16c031b436f60b82e64ea0a98eae398dde3620b1e8951a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4ba45378d2f35b3152409c3b40267ff60a37c6880476a1fc616ddd5716c4de9`  
		Last Modified: Wed, 16 Oct 2024 18:36:25 GMT  
		Size: 379.5 KB (379484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1868f8d087ded5c8fe49f55a0c4b620cfc4f66bf5ca9ab1a76c4720b231b41f3`  
		Last Modified: Wed, 16 Oct 2024 18:36:25 GMT  
		Size: 9.3 KB (9306 bytes)  
		MIME: application/vnd.in-toto+json
