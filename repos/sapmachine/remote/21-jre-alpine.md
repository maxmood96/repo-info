## `sapmachine:21-jre-alpine`

```console
$ docker pull sapmachine@sha256:e878d1b853f0b49f7257aeda7d4fb19e2b6dae40169b2c2e1530eefd3758c165
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:0952a1fcd69af8331817ee955c0d4f84ac2ca78c54951cd1c0f4ed6391325406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64086769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e193c276a45d9f46a16200cadb1cbc5ea77e8f6a59735946c17247fbe4fa183`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.9-r0 # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a199d85f9963512dfb842256637591637b80bf0aceda129b8fc1ed56bb018f`  
		Last Modified: Wed, 22 Oct 2025 02:43:15 GMT  
		Size: 60.3 MB (60284317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:995da158aaf37f6831369a3e8772a9305b4cb70a3f45334ce72a6ef2d3e5ac30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.1 KB (431102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6eae91462018fb9ccdc759ebff922dc3d24b156c67cbc8cd52b574233ff3198`

```dockerfile
```

-	Layers:
	-	`sha256:58f21cce2b2fed4d949b589febb3f8bda548e5f657ad3628395fa9d96a51d40c`  
		Last Modified: Wed, 22 Oct 2025 02:43:13 GMT  
		Size: 423.5 KB (423456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2047630e4fbb94f7304deebd6017ce200b04fd11d308e7151bccce82c9cef2b`  
		Last Modified: Wed, 22 Oct 2025 02:43:13 GMT  
		Size: 7.6 KB (7646 bytes)  
		MIME: application/vnd.in-toto+json
