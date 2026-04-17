## `sapmachine:25-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:75bf152399a6edacc5158adcd4c3cf8a123c6ab718ccbea621d69e6a9a675d80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:236ae5cbc11a3c3758f842ea7865db41af948de3230d1a20e1dee0e758bd564a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61791424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9afe61a2512780db111cb913456e19903310499b3213f2dea475debb57e241`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:27 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Fri, 17 Apr 2026 00:34:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Fri, 17 Apr 2026 00:34:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cfe0c99c4915efed2dbe298a67a2644b3073fb9320870881d510071aab0ab6`  
		Last Modified: Fri, 17 Apr 2026 00:34:38 GMT  
		Size: 58.0 MB (57983235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f0b4eb9dcdb015414070e5bf9385f3105f0382bf585a7c5066d420251de5b91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.8 KB (438796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e65d46c8d270717d75e971880949d69513375e43d5a73a3930e892f6d9d98e1`

```dockerfile
```

-	Layers:
	-	`sha256:09a4cfcfc8e3e17ec749dad7db046539f5b6684290375a2b259732ca3094bf82`  
		Last Modified: Fri, 17 Apr 2026 00:34:36 GMT  
		Size: 431.5 KB (431507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f8c192b66f26f068f40df0fce5d1ca076a5fba7714afd7d8329a2010ba9069`  
		Last Modified: Fri, 17 Apr 2026 00:34:36 GMT  
		Size: 7.3 KB (7289 bytes)  
		MIME: application/vnd.in-toto+json
