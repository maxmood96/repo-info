## `sapmachine:17-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:aba4169c3e20fdaf7d4f0f8e7aac234a7df19c44ed35707ff71a1e4a9fbc5233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:c446d95359abdbd448dd5bdc8b487f08a538a0594a53baf33604eeb0eb57b930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204294895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01d319d2570974600a641436ce6231f283580e0b301ebf432cd1360658e9717`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.15-r0 # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1dd4b26b52e88288d25e1f502b380d6e5a7f3dfd2b199c9dd1efb681cc300`  
		Last Modified: Thu, 08 May 2025 18:15:57 GMT  
		Size: 200.7 MB (200652648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:07b0e5c4014184ac5d74d1e87946a92c21cf64219c1b131520839fa0cc355edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.4 KB (516354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fa49bccbd1ce1fd1ba571ef523e22c3a5e8fdf5c7c0b9bf2c243a3bcca9e9f`

```dockerfile
```

-	Layers:
	-	`sha256:988d70f3b6a674a5f56b41934045526893cccd112da39ea95823c84cbd56388d`  
		Last Modified: Tue, 17 Jun 2025 10:23:08 GMT  
		Size: 508.0 KB (508038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aafc1bfbd849c298033cc81e2c30f22e3c5bb8bbafa6d7f2f3affc34e9d24d8e`  
		Last Modified: Tue, 17 Jun 2025 10:23:09 GMT  
		Size: 8.3 KB (8316 bytes)  
		MIME: application/vnd.in-toto+json
