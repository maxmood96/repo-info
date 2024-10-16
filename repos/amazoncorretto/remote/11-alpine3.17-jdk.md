## `amazoncorretto:11-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:ca9e588e456a0b5f12f8b8c410ac974004b6512e2b3b08d0e6907c673f875ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5ba622463eabb33259750e840c125fb43549383695e170fd1d7d5373644c054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145302449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c769d9510c84fa61a2241137fe6ea444276c36a915cdb497e3f2f1ef4fcd565d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:24 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Fri, 06 Sep 2024 22:20:25 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b6a0448b08e1f3df71d8534044a1f15a242a5381b6b2b74bbd207eace0f1f8`  
		Last Modified: Wed, 16 Oct 2024 17:56:06 GMT  
		Size: 141.9 MB (141910255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b618ae2cf814b2b5796092927d2e17d6a5f16894ac4e147f50000eb4b245d7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 KB (396184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd4266480320e2276abaa93bbe21e7f5c1d460e2adacc61f2805bec3fd35d44`

```dockerfile
```

-	Layers:
	-	`sha256:c58426fbfb902478d0e4182f4e27de54b911142dbf5ea6fa22a86e5108136894`  
		Last Modified: Wed, 16 Oct 2024 17:56:04 GMT  
		Size: 387.0 KB (386975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8440bea5b1ebee8be750dbe33b4d825f7af7b97f8cc79724898eaffb64b79aba`  
		Last Modified: Wed, 16 Oct 2024 17:56:04 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56749b0e0ccf3a8e763cadaa4e5ac875cbc261976ca6ec902030e75f7d63aca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143233737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce03d931969a49232e6f5543aa8a08f1d4b4b477fc505b332b4ac8a06b7220c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:e3f989df31d7e2d820078058c5d0ed7d98695c5b86bd172276270ebb59d75ee6 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4a3d188841b4b0359cda0d73dc5f89f8bc569f3bcb178cfd0507b4ead0db7bf4`  
		Last Modified: Fri, 06 Sep 2024 22:45:06 GMT  
		Size: 3.3 MB (3275072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466b3499e6868e0225dabacf196de5d083d275fd7e195c28ece84780a528d7c8`  
		Last Modified: Sat, 07 Sep 2024 12:08:51 GMT  
		Size: 140.0 MB (139958665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9667dd1a6273b8b23970bfa44458474f26f8fd7c452f6485f2330a6479e389b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00a77b16b5fc7d188e4cf66cf5feea50ef09f15e9cf13b9dfc726f72daa0e9a`

```dockerfile
```

-	Layers:
	-	`sha256:4f17ef8dc11553836377373ec66584aac0bbf23b172a3d1ab72af207319904b0`  
		Last Modified: Sat, 07 Sep 2024 12:08:48 GMT  
		Size: 387.0 KB (387018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bba4fe07be30ca18167537dce892f61bf16bc52a10ff6790e8169a6ddca9a61`  
		Last Modified: Sat, 07 Sep 2024 12:08:48 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
