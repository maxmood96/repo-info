## `sapmachine:21-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:4511a76d60ed170965b827d885ca447c8a68b15e4bd4751b9096e6ed8f3996d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:e300634821d13658801c660962d36413f03a5e6220d5c08fd1a5c229e3b49d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64653215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e9d59e9e993ccce1fcef3de0529e4a699080978776afc67e17563ccbdbe67f`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:39 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.10.0.1-r0 # buildkit
# Fri, 17 Apr 2026 00:34:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Fri, 17 Apr 2026 00:34:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf7458c82dd6e15e035034152cc117e159e8018c46513edb9ce53ada56cf976`  
		Last Modified: Fri, 17 Apr 2026 00:34:51 GMT  
		Size: 60.8 MB (60845026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95e7a5245a0e9ed11b3ebc1322ee6a938562a8d0ce5d1c53f530d3d57f9941af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 KB (433625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54572bc828577a98aa62e1f988403f2eae7b4a08e668acdac7710db16c7f3dae`

```dockerfile
```

-	Layers:
	-	`sha256:ed9bd61606e9377f3cbe89363934cc9de7b1f881a5c60e9de04a67b53bfdc25d`  
		Last Modified: Fri, 17 Apr 2026 00:34:49 GMT  
		Size: 426.6 KB (426646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02983876ee5196a1706f528a058fee818beb45423129aa60ed1b7bf29bff9b14`  
		Last Modified: Fri, 17 Apr 2026 00:34:49 GMT  
		Size: 7.0 KB (6979 bytes)  
		MIME: application/vnd.in-toto+json
