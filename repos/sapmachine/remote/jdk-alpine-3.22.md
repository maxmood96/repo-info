## `sapmachine:jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:37aed5d51541720268f0586ea0b4702ef57fbced49a16e78e5f277bf459d00fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:3af6cde84909b65685699a7128d793a33e0eec57d2180497bb581bf1c0f1782a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231580518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980afa3f4dadfdca3c1a495f274f7fc7e2c47c9dea93f215dd4c6f736fd8e960`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:33:38 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Fri, 17 Apr 2026 00:33:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Fri, 17 Apr 2026 00:33:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb38bd9dea5473daf1e03fe530b72da6174f642f04d082d2384ed283d6e97c73`  
		Last Modified: Fri, 17 Apr 2026 00:34:00 GMT  
		Size: 227.8 MB (227772329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dde68b9b7f0d8a13bdb676c9ffb17b873e99bfeb8de0ec55299c1b0f4499596f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.2 KB (506224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b315a456f0326f860830c6014df26c1370bab9ed3baf0c242c0188aba212e9`

```dockerfile
```

-	Layers:
	-	`sha256:46a10f4831a4df85cdb7fccfbcc9d72f9f60f219104f172163b95f3cfd3f3310`  
		Last Modified: Fri, 17 Apr 2026 00:33:55 GMT  
		Size: 498.6 KB (498647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134a079ebb601154cd194708ed838a8bd549bf54faa30692bc05ad520a91b05e`  
		Last Modified: Fri, 17 Apr 2026 00:33:55 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
