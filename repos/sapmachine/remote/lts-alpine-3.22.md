## `sapmachine:lts-alpine-3.22`

```console
$ docker pull sapmachine@sha256:1f8def65eba589f717e80f785d6a8f0fc0d44d0c5ac7fdfc261935842e8b13e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:49d2ada863dc51e330e42faa6c53de82abd9fee1282252f706f2514d38a74238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226797410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a2f4fd80e9a253d55910f67227c6ff50b2c1e9f2c3e49e9e2c27f8b8d65263`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:01:53 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.3-r0 # buildkit
# Tue, 21 Apr 2026 23:01:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Tue, 21 Apr 2026 23:01:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac76fd9cc84477144de56213f773b370557f83b72f0bbcfde5b51bfbeba491e`  
		Last Modified: Tue, 21 Apr 2026 23:02:15 GMT  
		Size: 223.0 MB (222989221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ab2dae789e2d3322afdc8213dcabbd4dc1f9ca76d4357ada35ce99755d6c61e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.2 KB (510186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4daffacbad50ea7a3a80475e4be84a1689bbe9b40b411f444b4c5297dd02f8d`

```dockerfile
```

-	Layers:
	-	`sha256:4957e0c0a69d16d95bdcf686c054c8ca22a24884c135e89f37062c5178e4ad19`  
		Last Modified: Tue, 21 Apr 2026 23:02:10 GMT  
		Size: 501.9 KB (501916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5e47af9c3ebd27e39642f9696039fc5b85d5545d06be879cc6805cc525c403`  
		Last Modified: Tue, 21 Apr 2026 23:02:10 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.in-toto+json
