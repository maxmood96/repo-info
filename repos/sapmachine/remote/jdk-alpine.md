## `sapmachine:jdk-alpine`

```console
$ docker pull sapmachine@sha256:035487111174afd34e92d3b5dc2ef4c8f4bc481ac98200420e8901cc2f921dab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ac06d5d576f37a423bad9f328c613f5f29e1790d39bae24b7bcacddbe04f386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236605691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8efcf9d8ad2f68d25ba6f6e2d95709fbc215da1265c815f3a8cd30e8fa587d2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jdk=24-r0 # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jdk
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee452d5e900533d152dce413648c6af44948489f00ffb9b29285ef1bbd89163`  
		Last Modified: Wed, 19 Mar 2025 20:32:57 GMT  
		Size: 233.0 MB (232963444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6754925f2ec40c7ab0d1be03324ca17ad04b0570af21bc7663b386615c47ff03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.7 KB (508713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edbe7eef2589b2656eb48dbf37c4e22b1bb3b33511c0efcc7f09ad40ff3bff6`

```dockerfile
```

-	Layers:
	-	`sha256:d12d31e0441274a7c05302c6e9a03a45fdde9eca94399278fd6f6a5f36829069`  
		Last Modified: Wed, 19 Mar 2025 20:32:54 GMT  
		Size: 500.5 KB (500459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128e4cec66b2433562ce00ec856677b33d248b7abdd259a73bd5422d71a6903e`  
		Last Modified: Wed, 19 Mar 2025 20:32:54 GMT  
		Size: 8.3 KB (8254 bytes)  
		MIME: application/vnd.in-toto+json
