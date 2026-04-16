## `sapmachine:17-jdk-alpine`

```console
$ docker pull sapmachine@sha256:5214507488f240c046a1617d2f70c4afcb88ba394381eea9ac07ab382a8f24f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:bee41633213e66fa4c65812c0ecec4f4bd53052823c5c867335c4c4783fb8ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206623550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116804de424cd6a468ff0f7067ee09d0061578aee6d55b9e8b56114744a9977e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:00:26 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Wed, 15 Apr 2026 21:00:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Wed, 15 Apr 2026 21:00:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6e6736ecb6831130482f598bb10ba4a0091f9737551a67a1eff34e77353ab`  
		Last Modified: Wed, 15 Apr 2026 21:00:49 GMT  
		Size: 202.8 MB (202759361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fde2703fad588cc80e4c312136c8b6af88e514f9d908c78437949a359e05f23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 KB (520922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8caae13861d42da270ce007c959968030bd3fbd85fb5406ca4f471c1ca5cba`

```dockerfile
```

-	Layers:
	-	`sha256:30fc50285848cc525547c13b9a4ff23468d0ac5d72d45cfc107208dc64f84fae`  
		Last Modified: Wed, 15 Apr 2026 21:00:44 GMT  
		Size: 512.0 KB (512016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca8d2fb074f50eef12a542c69c8c6e2f0e67655123c97c13b51b2e1ddab5ae6`  
		Last Modified: Wed, 15 Apr 2026 21:00:43 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json
