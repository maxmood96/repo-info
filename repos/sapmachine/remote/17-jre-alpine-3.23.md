## `sapmachine:17-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:bc2cd7d17670a64122068fce8d50df8a69c60a74dc9d793e8a4acfeef5e3508e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:7e423a034560de9fe4c947067641b041636092e2ab6fae8c51b6dd21d55e0f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59365514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7545f1ee49001b1c820fa6b336fa1706a1729b2993800b7d184c6200868400`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:05:42 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.19-r0 # buildkit
# Tue, 21 Apr 2026 23:05:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Tue, 21 Apr 2026 23:05:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eab32c493027bed4925f08ea8c40bedb1eb3c953c70ff101040ff261782abbb`  
		Last Modified: Tue, 21 Apr 2026 23:05:54 GMT  
		Size: 55.5 MB (55501325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:65052af4af2ad028559e6a0a6d5d574b4c09ce6cdfb979e7ffe6d6c6adeb30ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.9 KB (434906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073378e2a9394a7b1294e8a4315866843c3a14afdf7ea7a646e39563da14227`

```dockerfile
```

-	Layers:
	-	`sha256:fc0fe2751b0ac001c5bb5c5342b07f6a7b4672f57147aeda05b59e8cb84b951b`  
		Last Modified: Tue, 21 Apr 2026 23:05:52 GMT  
		Size: 427.3 KB (427296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e3c6afebbd8fd1996d98fa4112b7aadbc71a48f697d99b088208d7e626a3ef`  
		Last Modified: Tue, 21 Apr 2026 23:05:51 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.in-toto+json
