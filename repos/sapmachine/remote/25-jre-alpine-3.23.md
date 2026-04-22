## `sapmachine:25-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:b497f015ed7bcccd0ccd8234b391131cdf39bd738db59a5bed98b5a5e72316e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:f111fbb8466da1df7104846008fb554a0966f425dcde2e12656c7254a1745d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62348525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af669de4804cf5c05928d01f94a5e847ffc2f309dd65e9b0537e41ac26943f2`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:03:55 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.3-r0 # buildkit
# Tue, 21 Apr 2026 23:03:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Tue, 21 Apr 2026 23:03:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d830cf19b9a64746afc73cf8a4f654f2b089439f63fc9f2cdd879fb5144f238d`  
		Last Modified: Tue, 21 Apr 2026 23:04:07 GMT  
		Size: 58.5 MB (58484336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d56d2f60a7180218531c04b7fd2a1f539443c24fb1bae5dee486fe9f956da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.0 KB (442036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40a2b4cf9625e72ad9a5c7e4204f4dad674e9a3835dd351d76f584091a69d90`

```dockerfile
```

-	Layers:
	-	`sha256:22f947527eb25708ed17581701ea505d4f2602108c3e153a116accaa4b4b47b2`  
		Last Modified: Tue, 21 Apr 2026 23:04:05 GMT  
		Size: 433.8 KB (433777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d8fc2dddd2ae6c4378fc3ad4c703169603b2b97be32266c1e02a0eddc137d2`  
		Last Modified: Tue, 21 Apr 2026 23:04:05 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.in-toto+json
