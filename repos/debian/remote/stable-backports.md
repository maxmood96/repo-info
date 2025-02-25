## `debian:stable-backports`

```console
$ docker pull debian@sha256:0868d354f0a5bf209df0138f1efb641f1841e78ee86cec060c250b8482e63303
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:a099f8abfdf084f6357257ba7525e94bec7d234fd5e742e59cff631f0fec66c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48476326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69961fd662c9584aa7b1b32d945bf1c211842cbfaff410fdb8bc7e527e24fa95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:319cc5f9a689830e5f0a7809e274e9c063c35f91cb5d0e2371f59f34a7446bb2`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 48.5 MB (48476103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce74608763aa23ee2be10e4efbf03dcc7f8e43b14dfaef19374a38b8c951c293`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ce2f4a556006a9d7c508138d0f4d10e6b5e5a2517e0b79dd48450def237e42ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d180544849a2898d632b0e434a2ebb3e5de6a453ca298d6ea4ef610cd79273e6`

```dockerfile
```

-	Layers:
	-	`sha256:71579cc38d81353e5fac1334dcaa8e1fc88f9157791f24d61bb41132de2a825f`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 3.6 MB (3619224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8bf2a236c5238638159199edf4b5c3e31f650c047d299b139180dd3771aa1f5`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2386ba4fe6e9e9290664ef64e6f424d33b8394cd07382c68b9475a89a96349ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46006722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc79af850677c795d67b5ef04f31fa50e97ff9a85df871219fee73d821c51365`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1deef512c1e98299304b8e67bff03de852668b74578ed1745161b76f16cb8e15`  
		Last Modified: Tue, 25 Feb 2025 01:31:58 GMT  
		Size: 46.0 MB (46006501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a35f5fb392c049534aaeee32bea4490ba6a4d0def7d119a7d4536c038b2c6f0`  
		Last Modified: Tue, 25 Feb 2025 02:20:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aff08b18e1a62652b15a79198faec34fd7b7b2fa38f1fcc43457b2063651ff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe41cc0a426a5ea2a1365b82cb1c42d3ddf1f2da328f1d30be844a42eee06343`

```dockerfile
```

-	Layers:
	-	`sha256:31f8c2f2e18b5fd2a8866343b815ca4a7cf585a7591c2630a1afb04ed7fd19f9`  
		Last Modified: Tue, 25 Feb 2025 02:20:04 GMT  
		Size: 3.6 MB (3619425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5876d728e074e5e1e372461fc482d24ef6a4ce63b12a94d3c865520bd13e9a`  
		Last Modified: Tue, 25 Feb 2025 02:20:04 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:701fc3fce2103d289d8382612df57753e4685cf33797e68ad340bf75f2bdac1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44184275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2569c98ae77c4bc97c2e3d0605493f52fb51d8f13f959d588fc84bf61fed52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:67233f4ea6c9cb8cfef1bc9f23f922545d9c94c02cfd1d0dcb6a972fa303193f`  
		Last Modified: Tue, 04 Feb 2025 01:39:51 GMT  
		Size: 44.2 MB (44184053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec94b895f770fcdf817ff97461600becc583b616d046c35b2b5f455ca6fdaf`  
		Last Modified: Tue, 04 Feb 2025 04:38:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:30e0e845bbba9a5353a6bc1430c92e2774291463918299b4ff5e1466ebdfd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157a1d73a424f005993b94fc574b656e6cd4276392ffac34402b8a1eb6bb56b`

```dockerfile
```

-	Layers:
	-	`sha256:7e127ab166677a703af4334ee3e2d844880d3eff95c25c8f5258735646cb608a`  
		Last Modified: Tue, 04 Feb 2025 04:38:42 GMT  
		Size: 3.6 MB (3621385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eae4a3d241fa41c5213f48e72b8c524064517a7a56d163b7de34a6e573a5ed5`  
		Last Modified: Tue, 04 Feb 2025 04:38:41 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d5267ad5eba2abd92e3eaecd0deab01da76bf723af4073a9eda52eb4110fe5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48308233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ba90b09538cfb53dd0be698badf91252fb06ca866dc150e07b37bd930c115`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bc50a3b87241d2f15e157de1ad359ab03ec88196efa05d44e62fba74bb7a7791`  
		Last Modified: Tue, 25 Feb 2025 01:32:48 GMT  
		Size: 48.3 MB (48308012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a889d6d89557d7ee7348d3a565050f12e67199ef06b007835cb5f9a2d6a19c`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:14ba3d411ff6759b0c03fa1e9f7d2a847fab922738635760a5f7b12a921bcd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38421cc300fdc2a3d087b7a9bb676ca69aa68ef9ec5ed062c3cd8d01a5aeeb`

```dockerfile
```

-	Layers:
	-	`sha256:6e51c1798bc433e64be1a267e4c42a3f3722294d66662272a57112101f7503f6`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 3.6 MB (3619439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a754b00e8a8593b9d1e64c5cf103bff8da0cba572862e961f28405abf0cb6601`  
		Last Modified: Tue, 25 Feb 2025 02:16:54 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:444ce24ea4dbeb15df6895655cd7cb275dbd75fc79cf876dd212be0cf4aa5cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49458675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740f1b5e9c536bc884c342808482901bb0accb0e55de89d132edc89419cfbda0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b329e055420506a8299aa9cee76ce488007de79a756a9aa86695471b9bbad57f`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 49.5 MB (49458455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cdf9bd770b983aed25ae13daf4c715cfb8851333849f2991e59df2b565bc0`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8fe571cd6fa886b45c46552607b575c1c148f6a2b3fd1b93178a13a6fa3fffcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be93fe656b660ffd907434a5a21eed913fc6c22847e47a9228bd16aba2309a18`

```dockerfile
```

-	Layers:
	-	`sha256:db22e327139ddef99370d38d84e0ee53ca716c31a683f158197d8089598dd994`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 3.6 MB (3616385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aee29e40022a2ff121982150414ed57a315d42b2a77512e90f1ce50b9168ead`  
		Last Modified: Tue, 25 Feb 2025 02:11:39 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:05cb37de7e0f1e1bc0b1539c6e25e06bf213c14e39333c2b2ac2e9125c8d5edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48759215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5122d68884508d45553fbeaf4e2528cd33d6141a36855aacf36f2d0d75acb215`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b00717954dcfd9e14c301b7b40373054eb7ce9750f649a121bd9a1709d351715`  
		Last Modified: Tue, 25 Feb 2025 01:31:54 GMT  
		Size: 48.8 MB (48758992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206ee07eea4cefc18424c245183a2b5518d7447d7b8e3497b87692efe018922`  
		Last Modified: Tue, 25 Feb 2025 02:14:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3f63d9ee11937fdc90aeda1837792eaced6b17f023f133db6eba2682d08f2385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f5e974bb8b30e051a9e22ff18e674ac725e70ca4b39195104b00b6c7d7ba27`

```dockerfile
```

-	Layers:
	-	`sha256:59605375e94f94b7a81ea3b733659c2459efb3619b7e789f8d48a7d94ee9b210`  
		Last Modified: Tue, 25 Feb 2025 02:14:09 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:87ffeb914b44d02f9743d36234bb929eb17218a86f2f8a3af54273635da99647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52307879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54910bcb4037f9d30d5342d0c1b2e82d4546b1adff676376d5bad1d395fb5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:76ac10ead5cd68e905a2bb06901683d02f01c7ed1e78371629895f251b5083a8`  
		Last Modified: Tue, 25 Feb 2025 01:32:16 GMT  
		Size: 52.3 MB (52307656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d499c867f40e7f0976cd9300f8d61bd9b7ca38e4263266b6534dc6768483bf`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:da1c7d62eb6c811de181eb52df44fa76de7a02e0cb1a7eaf061476cbc3fedfa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86589a487992c4752ed4c3a980669da661a2218c3c45f2c0780e15bf0e0a98b`

```dockerfile
```

-	Layers:
	-	`sha256:e5925fa459d0b141ebaec57f5a6736db450a0ca5f4627c50b1f84db9745bfba2`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 3.6 MB (3623484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23a782b2100f7ef871781496e7ca49ec0d039a72e5b4d06a39bac654a88b974`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:725acb97c4b43d757ed862d296b1786b30bf637334805b83419c81db4da94fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47130215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca435e19c69bf504ad13fe8c5d9e08246d706476c9b270dc24d8dfee0b3a9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f7d27d237065ed06ce13b57f4617f9db17930f64a7977c5a049c2db3b7571af`  
		Last Modified: Tue, 25 Feb 2025 01:32:01 GMT  
		Size: 47.1 MB (47129994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d362dfaf3ab83dfc1b31675ab9898063a8a3dcab92a94dafac10e64695b51ca`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94e298b935948cdeffee1538f9ddd004781cb85ea564319afda2de24fb9b2faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f869f8932b45e390d121bccd15d2b47e5407288699449979d9f9ccf7c2f15dad`

```dockerfile
```

-	Layers:
	-	`sha256:4abf790762cffdefe1994321ba5dcf009690f98e0008d1df8f241a75f772152a`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 3.6 MB (3618954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ce047bbbbb867a3e1fe9de4c6d576382c8c961607d3fa2083b068761c6ac1e`  
		Last Modified: Tue, 25 Feb 2025 02:13:31 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
