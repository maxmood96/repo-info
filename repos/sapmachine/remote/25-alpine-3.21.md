## `sapmachine:25-alpine-3.21`

```console
$ docker pull sapmachine@sha256:a1ce0e61bf9efb6440b31bf1915c6af0e3cfd94932d3471dca3c3c72aa30e465
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:40d4dd25ee3c693f7ebd94a5494de653ff5eeb1c1a47f63103ecb6067a2843db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238341109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350fef8faf05aef3af05dfd215f794a96541dd56b26ded9d18862b46f684fd89`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d9210704221c2f4acf52f498db49e60811b11bda3a6e1a167794237002b179`  
		Last Modified: Wed, 08 Oct 2025 23:20:13 GMT  
		Size: 234.7 MB (234698540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b40da5303301882d0fb5d4d3f2556919bfdf46294488f7eed1f59a4eb9948c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 KB (511069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d3625e2ad57ddcaf1d6f01e5f7c15d235e958edcdb1b1dcdf8ebdaf329ef6`

```dockerfile
```

-	Layers:
	-	`sha256:150a0f6248850c84de34033935e1d80bcb020609573e4803c4cb86f889adcdf4`  
		Last Modified: Thu, 09 Oct 2025 00:07:06 GMT  
		Size: 502.8 KB (502792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa1968cb827d0cce200ec1196edcec5d38ddee723d06ac3f450804926661594`  
		Last Modified: Thu, 09 Oct 2025 00:07:07 GMT  
		Size: 8.3 KB (8277 bytes)  
		MIME: application/vnd.in-toto+json
