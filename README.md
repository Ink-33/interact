# Interact

Package interact provides implementations for some basic interaction
that aims to make cli program a bit more pretty and let it easy to use.

## Usage

``` sh
go get -u repo.smlk.org/interact
```

## Demo

``` golang
func main() {
	cmds := interact.Choose{
		Title: "Select operation:",
		Choices: []interact.Choice{
			interact.NewChoice(
				"Choice A",
				ChoiceAHandler,
			),
			interact.NewChoice(
				"Choice B",
				ChoiceAHandler,
			),
			interact.NewChoice(
				"Choice C",
				ChoiceCHandler,
			),
		},
		Loop: true,
	}
	_, err := cmds.Do()
	if err != nil {
		panic(err)
	}
}
```
