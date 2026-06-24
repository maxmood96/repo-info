## `debian:trixie-backports`

```console
$ docker pull debian@sha256:65ab535e1271210395f3b53928f9a836ee3128fddf296de1ced641ba03f9f913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:68713f9d555355139b594d46866b18d5fd00cc23d9b74ab8d6a980f5e42d899e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49317344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3152c30b28f63611807a32b6fa48bacbe071953ddfb1a7b3a06febeb5076c66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:26 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3078aa1de4195b56a5d2a4dba6c639f4d6a0084cde3e3dd35966cf09e5aea7e2`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d27f70220f902e6c05c663bcf5a8fa3d6e0987572cea8752334ddcac83d62415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e2480e2d919e51c4c4d82499fb3757c51a648ebc6191567afb933fd4629261`

```dockerfile
```

-	Layers:
	-	`sha256:c96f6d8a45233c2bf6e021878acc22dd780cbad91777008af9567ec7564301c2`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a6d2a8ab77bccd68d5f43ebcfdcf2409aa683ac324184d059d3c72fa6e2c02`  
		Last Modified: Thu, 11 Jun 2026 00:15:32 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a3ba6476590c427ff2d5cbade5cd8e128ebbc8d752782dd3c80382e1f83cc75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47495033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e576fb12538ceabc3ad199c86bdcbd645c5bc354dae401078507f4b6b49d9ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c7aec27d8d7251d4ab1e72a48ca37d3dd7b38c179ba32a129512e1cbaa7c45`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:55e42476250d5bdff7e92779e48c6ae8e3867f2c37db6f72f54365bb82636e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d0b13a59f94fa70751d3e0992df69d05f797167e42af483d854332b2d4dd3d`

```dockerfile
```

-	Layers:
	-	`sha256:7733c3c1cb0c8f65fc1bf8982ede1e3b135cf794b27568e395682b11464d579d`  
		Last Modified: Thu, 11 Jun 2026 00:16:13 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ea2d430ad569073fc062f0ce469d466194a6ace46f25e37c01556f80fbb5af`  
		Last Modified: Thu, 11 Jun 2026 00:16:12 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f266e2daf2c99a781df2491d5b28794c11a3cfbc631f63118177e64d5d2e9d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45748865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b5943ce6a6482dea9a8dcdfa6ba1ea112f4e48a5653e3d58fc94175ec9e7aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ed6609305b4406dccd7df3eaa23566e8fbca377df7f71b6e93a4204f3dc65`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4be321ce65dddb97a260a71c087a59c3c34d83259be069d5c8bdf85acf0263ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a53cf8c5a2b3a09179f521121854c93b79856af265d33824ab8669e85cde570`

```dockerfile
```

-	Layers:
	-	`sha256:a56c623e21efe5e5f497657d86a49510213bb4430ea0f3f45ee225c81f988e63`  
		Last Modified: Thu, 11 Jun 2026 00:15:39 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15eea470f37a15e2dfed271e3db92a216a2414eac6823297a0c89774c73f8c25`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ccf19b17558e4b161d9e46b024e78bcc2b240daf935f99529d9196707576063c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae5dad9c6e4b823d82292a20367a9fd87314e504c22bc94d81d5d773ed13c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3765bcd17e740df4e50d048dff74d9da573fd433946ba267483f43b8784488`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6587eb66e0e91cf3cd22522d91c9dc36f9bd124b085e3e4e9ff454f0afb43e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a09120ec3ec6b61b1d9d5358dd8e221da148056d41bc033934b8c7be558022`

```dockerfile
```

-	Layers:
	-	`sha256:f6f0c637929b2627b36098de220bab9510cd99f860097643a918cd79e272fc36`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39508f3253bc0245bc6d4c8bdd4690866b40c4500c2d71c3f7f0dd2f2401eac`  
		Last Modified: Thu, 11 Jun 2026 00:15:56 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:b85165591d06952f64065548072bc815d0fecbdca063732405e12d641e82a15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50835878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ea81ddc37f428a45f873d603d1c319c6cdcc95cb0a92c6cf0f55b6398c98a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ae12c2ff3fb5df23b854f2a97ab858f54bb2f71491a9276fddf8be7e76d3182a`  
		Last Modified: Wed, 24 Jun 2026 00:28:34 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53682b0b3a28f4e1d1fbfc32f157153660212403f55e5bdcbc5ce36a338007`  
		Last Modified: Wed, 24 Jun 2026 01:15:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:06e4a6a834807a452a0d34942d93a8843537bc8f19d0ab7d91db147a9ed61a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930340f5dd5e2c6d66ec137b4f8a4c51b38df93247755f0e97651f579b91873`

```dockerfile
```

-	Layers:
	-	`sha256:d2b7e0a1f33c90e49f9a0f2f5a993a084e367f5b862b369bce81ff04501ee141`  
		Last Modified: Wed, 24 Jun 2026 01:15:31 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8dee2577d43e7caafe3f710475d84f4b4000f90d354721e57dbbdfdca6fc052`  
		Last Modified: Wed, 24 Jun 2026 01:15:31 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:99814b99f1d70897064e59a2d89c3cdb1f8d9fb2c32fd98f9b7435e1836b7e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26200b0a6e8f9870dc22cc50277888c8bbebb93d0d97005580a8d31fbd64e987`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:04 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbba26ad88e4aa609a90fa8fe15720190ce35f7bb40874d73e54478e3873d7`  
		Last Modified: Wed, 24 Jun 2026 01:15:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1c0a0fcf2ae998d6020340adc0c22c9cc6df4a55b1b6545a21903774632c3e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c7c0990c77a52b44638843eff8587a3dc7b4b1cd9e9d142ca545e824f5360a`

```dockerfile
```

-	Layers:
	-	`sha256:3032cb055942c612578a5e9185cefa06ec68c31c34436a63b7a98097fb74bca3`  
		Last Modified: Wed, 24 Jun 2026 01:15:20 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5f3eaf499929aa383c48dc4c22ab2a97717630cf8c76c021d1ecbc27df4a11`  
		Last Modified: Wed, 24 Jun 2026 01:15:20 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2aa26744b98c34dc761adc969cd37c9581ecc38d44ee7b69915fdfb85c582cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47802763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374c7996827bc0d490a13a64ba4f4e348e4f14e2c1e90e06f935e6a365e37c27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 22:12:23 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5d828555072267505fd8c01bd511aa2e85b57db4591d7af1c1c5df9ca568aac0`  
		Last Modified: Thu, 11 Jun 2026 02:59:31 GMT  
		Size: 47.8 MB (47802538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf2de462e1a29cd6ebb0f8cef2a57d9cef0d9ca0daef40f3bedf2236ce7685`  
		Last Modified: Thu, 11 Jun 2026 22:13:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d67448beff44992fe07f730f4ec47fe5972cdfe0442136786feac7bd3b23b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab4ee64b4083f7973a320025ef8c694a8a6e9223f3e76cb383a37d893494f8d`

```dockerfile
```

-	Layers:
	-	`sha256:ff569ed0a9f0ece35c8bd98463a4b49a5f662306557809b415b1302c53dcd690`  
		Last Modified: Thu, 11 Jun 2026 22:13:17 GMT  
		Size: 3.2 MB (3163280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:423d2c1fd6475ca56519b82f92575b9fbdf6e636d7d42446dc9c0994f2f2cf1e`  
		Last Modified: Thu, 11 Jun 2026 22:13:17 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:059e1bf0df94dae535663bc93c6eefa6e7338f669b8bdd0b35b8e042f6fd83b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49386283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a2c1289d46fe578fa452608655de6675408500061e9c6b0e30a650710dceae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:27 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301d7eb41aa1a0fe87a5efdbe3348d13f5057e00c5d6ef78380aac79eeb7b325`  
		Last Modified: Wed, 24 Jun 2026 01:14:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:29a60be8b6c81ab29b92f883aeb4827882bed1966f1a810995404af63559444e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1007ad85d57dae0e0dd0f8fe394c2971f51f612b534a073014646de20945082d`

```dockerfile
```

-	Layers:
	-	`sha256:5170b852a05e7d41b9393987e1d33d130932ec92e4cf116d3e21944b241de95a`  
		Last Modified: Wed, 24 Jun 2026 01:14:37 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939b26394a55f1d04e5bac50296687375277033c8d8ef4d66c746524cf13776c`  
		Last Modified: Wed, 24 Jun 2026 01:14:37 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json
