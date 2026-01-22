## `sapmachine:lts-alpine-3.21`

```console
$ docker pull sapmachine@sha256:12e83c79514e81ca0e3e90a9885968726db1e45548b0d79a04ed91fd851becdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:ec8fb13adeaefa6dca18d967381cbbbfc60cc8898b89efd2b93bfd207d6c3ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226256652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76253efa3d8061200472ee1015e5d12ab34f2438e92f881f7c7467deb307f5f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:02:41 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Wed, 21 Jan 2026 20:02:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 21 Jan 2026 20:02:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b602e59b22571e60c5cf60a44f958025dc0a7703f17830ac2adc42a01a22b9f7`  
		Last Modified: Wed, 21 Jan 2026 20:03:02 GMT  
		Size: 222.6 MB (222614083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e616128fac17796f1f69cadbdb601eae4f7a9bcc958c32878d4085f2bbbdadb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.2 KB (514245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d0ec279db810d532e6b0bcd7432448a1fec8b9425ed516dd9c3e7fca3077f`

```dockerfile
```

-	Layers:
	-	`sha256:b2c65bcb5ac01391b3088a3855a719960fa4e7d31ce4845cb94f797a790d7bb9`  
		Last Modified: Wed, 21 Jan 2026 20:02:57 GMT  
		Size: 505.3 KB (505335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9403dd718aef612e87eed10ba80862897b38e9fa04fa654580b5d6c8e6203b6`  
		Last Modified: Wed, 21 Jan 2026 20:02:57 GMT  
		Size: 8.9 KB (8910 bytes)  
		MIME: application/vnd.in-toto+json
