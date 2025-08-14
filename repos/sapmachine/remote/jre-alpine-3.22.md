## `sapmachine:jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:10c1d9e3ea86282d13911ab89a368a0be78706db7bde41c7dda73f0df6b4e540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:ce0d0c693f45259a3aa8896f948b1af4c00a8e829615efe5905558db5daea355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71894252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35cd3812959e0fb2936ea4b621598e671fc4710fd29430618d53425ba902b6b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jre=24.0.2-r0 # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jre
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09721b2c11b1de4b4c9dbee2410254223c2c16748b20fb2dfa7c45c5ab1ae96b`  
		Last Modified: Tue, 15 Jul 2025 20:45:55 GMT  
		Size: 68.1 MB (68094563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a5bab7eb1ab62c6b9ba0038eaf9e85fd354642f5e140913eb97e0cea2f1521b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.2 KB (441213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc956d56588720c591031d7d32c961fd1cb6ff10dbce1986b7e5e1c5d46e3b1`

```dockerfile
```

-	Layers:
	-	`sha256:78acc28ad2ff4b22f91b7ad194392da471644bbc694534334017fb5807b0ec2f`  
		Last Modified: Wed, 16 Jul 2025 00:10:08 GMT  
		Size: 432.9 KB (432925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07339d4b8bad131a59a10c9dbd70a1345958f8585eacca6b2ec12cb9425cf63b`  
		Last Modified: Wed, 16 Jul 2025 00:10:09 GMT  
		Size: 8.3 KB (8288 bytes)  
		MIME: application/vnd.in-toto+json
