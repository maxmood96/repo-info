## `sapmachine:jre-alpine`

```console
$ docker pull sapmachine@sha256:6e1c32d9c2ba61a753af9b64d098412275ec910b38dfd06c20587a1770c31485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:48b04e2da63e72b1bb7160bef9af956cd823f8370338bdbfafbe9a6159c2a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d19684a8f5409ab54f70b0b09a07be8e432408f6e0a9e1060181b4f24ec987`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.1-r0 # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f07f8e3ee345637306649db079868eece2d792bda0f4a9fe7ce87d1fddbfda`  
		Last Modified: Thu, 01 Jan 2026 16:33:45 GMT  
		Size: 57.4 MB (57439685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:698b650c13a441c354b2331cebb0e60b3fa0620557c4ab24a59858ea91f242a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.2 KB (438246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591fc6dd8fb20855874b91ee6dbe01753d50ccce8e69d04bf4a6dd19f3c915db`

```dockerfile
```

-	Layers:
	-	`sha256:039759218b593cacc011787f0fa0ddef9b9077eff22fc48eb3dcdf4f7f1a9537`  
		Last Modified: Wed, 22 Oct 2025 02:42:06 GMT  
		Size: 429.3 KB (429307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0705f2f96a2011ab5ab938eb6a8c9a89f45cd875d180603ebca0f22d12fa015e`  
		Last Modified: Wed, 22 Oct 2025 02:42:06 GMT  
		Size: 8.9 KB (8939 bytes)  
		MIME: application/vnd.in-toto+json
