## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:4e18f10d8007a2d3d6eb517d9035656aabce4f9ba9c946d1d2582e3f8875649e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:58c2784fcdf97a6dbcddfe8f783b7376630e9cea3282d64111f9724e8b497a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145571820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d8091f8c60c3206597812e6ecc4ebeeeaf02615bc0cecac77036a612a20e50`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bbdfb73657a1ed3820dbd20a06713edc0063de8c1a2a26cc8975cfbbe093f5`  
		Last Modified: Tue, 15 Apr 2025 23:55:32 GMT  
		Size: 141.9 MB (141944923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:909f92fe7603a2949d1797be62d22ecf5f30a6040075eba71add6e52ececc604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 KB (392880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de12db06dbff0dcdc9a236a997e5f848135b71db948990e574b6a09bf523844`

```dockerfile
```

-	Layers:
	-	`sha256:6f254f148bc59e2e37c41b9ef882ee309642de99afa001795cfd7564f3c9799a`  
		Last Modified: Tue, 15 Apr 2025 23:55:30 GMT  
		Size: 383.5 KB (383463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c434dd165a1a8077b4015e0f9fda26c89ca7f42ae8467186731847d81767122`  
		Last Modified: Tue, 15 Apr 2025 23:55:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8be02e561b719e18074fda3926ece02945a02409503815a7863dec116fc62e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144125985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fda89da8b871a3e1352c8c82442cec541d5664a52694898eeeee31563ec9ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f1dbc5b487ddd138799e7ad6976476cfdbb7dc02e25c0c3078775ad516425`  
		Last Modified: Fri, 14 Feb 2025 22:35:10 GMT  
		Size: 140.0 MB (140034820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa859f406d2353685ef0aa78417cc83e4486defeba21c871df16342b7251c940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.0 KB (393039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28513b754731a722b69bc68364ffca884ddc8564b0514a2819a95dffee551cb`

```dockerfile
```

-	Layers:
	-	`sha256:1778d012cdcc934c0cc589a27b131b80e2e144e84055a3b06461e34e1925de42`  
		Last Modified: Fri, 14 Feb 2025 22:35:06 GMT  
		Size: 383.5 KB (383519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4956d35f5a3796d6561aea45b3380732b58b6d13c16fb04e09dcd5f2da3f21d`  
		Last Modified: Fri, 14 Feb 2025 22:35:06 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
