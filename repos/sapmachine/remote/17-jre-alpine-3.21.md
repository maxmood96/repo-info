## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:8471f5ac8db31c098dcca1f265ac018800b98bfbfbb3b30cfc495909c25cd2e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:80694055fa31623ac69584904dc009bb175015f45a064dcce2bb8c6332280861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57958274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6274ca6d3d824cfc68e0db13329f859175b425e7a35907db1462aaa4c74646b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.17-r0 # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253c63cbc09e1cc24abe5571b4f34de0ccedff5be2ecfd09e0ab900b5a253a84`  
		Last Modified: Wed, 22 Oct 2025 02:44:22 GMT  
		Size: 54.3 MB (54315705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d43d040bfe97170914eb32ce9b9e1e3743f862f725af06f192be471e59b18cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.4 KB (429443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a931a0d349bcd5a2d2b01db912cbc90c0240f35c78b32e1734572ec448e5ed`

```dockerfile
```

-	Layers:
	-	`sha256:08bc707d4281e6548bf4945a0aebe017e3d7aee9780e14502ba08e55dcf48c86`  
		Last Modified: Wed, 22 Oct 2025 02:44:20 GMT  
		Size: 422.4 KB (422440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fc6b86d127c5301aeb08489b3519660c279fdc85acaa87a15b19db6151d1ae`  
		Last Modified: Wed, 22 Oct 2025 02:44:20 GMT  
		Size: 7.0 KB (7003 bytes)  
		MIME: application/vnd.in-toto+json
