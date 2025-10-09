## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:15da02d93e72b9f857b711192f02931efd28ad8dbf66e6118a2f8ba879e052a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:a15c3fab7903d3c34deedc351bc7f73975862efe5064066e5444797cf2cd267d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63779571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d88dca21f2aff9b3a50f58e8553dc2b9605977eb575cbb5fff884f3f93e6914`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-21-jre=21.0.8-r0 # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ecc702209dd9c5c48955262d1e2a42c639545aa1f3fdda7ebfeee6b422654`  
		Last Modified: Wed, 08 Oct 2025 23:21:29 GMT  
		Size: 60.1 MB (60137002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2ade1dc124035bb528fd5747c01eb6abd168b44d84c74435f2492c33af9c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 KB (430718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6185e137e05d6a372c4a4c1b784e702ffa096d840c2a3e963868a57daa777be`

```dockerfile
```

-	Layers:
	-	`sha256:9747a5bc7dd971c35d90b16aee620d93d895141be79eec4a70df78376f3e7e6e`  
		Last Modified: Thu, 09 Oct 2025 00:06:15 GMT  
		Size: 423.7 KB (423710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dfc5121fda2d2de0ba8368a3d4f5a3caa8c0e04c2c2cb1893500e6a72d3ff52`  
		Last Modified: Thu, 09 Oct 2025 00:06:16 GMT  
		Size: 7.0 KB (7008 bytes)  
		MIME: application/vnd.in-toto+json
