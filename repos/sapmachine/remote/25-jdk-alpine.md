## `sapmachine:25-jdk-alpine`

```console
$ docker pull sapmachine@sha256:c4a5cf283534141fdac8bbff13f000027a36561d7e140a0a5d4d5c3dd97793fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:dd157864e7a75496791449c3ef66649ba5960934afe8de9bc63bf92374184139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (227015333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056388ac6583e520b6c14259ff0aa0e3d48e9d0f6a7c9373f8a1596cbaf5ec4e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:38 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Wed, 18 Mar 2026 17:50:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 18 Mar 2026 17:50:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a41985b3ea013937f50c8090625349db488f9dd724db90bb7e6fe70470bea`  
		Last Modified: Wed, 18 Mar 2026 17:51:00 GMT  
		Size: 223.2 MB (223153512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ba72b300dd648ffca3c334fd3835c0df485f313e85c8adf6b7ec2d24efc205cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.0 KB (514004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca17bd4571e41add1991a4f72cb52cf52e36451e2ddfed072f40693938d3d05`

```dockerfile
```

-	Layers:
	-	`sha256:fe2bc9dcbcd127d68be66f69672a3c425fc04e22aadd27e05775b2bf127e37f6`  
		Last Modified: Wed, 18 Mar 2026 17:50:56 GMT  
		Size: 503.8 KB (503818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c18b994eb5f5ce543e93db302e9ce54d1897b3999022d2ba22b840ad4464dd2`  
		Last Modified: Wed, 18 Mar 2026 17:50:55 GMT  
		Size: 10.2 KB (10186 bytes)  
		MIME: application/vnd.in-toto+json
