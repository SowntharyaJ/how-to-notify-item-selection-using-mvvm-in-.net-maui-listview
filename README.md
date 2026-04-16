# how-to-notify-item-selection-using-mvvm-in-.net-maui-listview

This example demonstrates how to notify item selection using mvvm in .NET MAUI ListView (SfListView).

## Sample

```xaml
<listView:SfListView x:Name="listView" ItemSize="70" ItemSpacing="0,0,5,0"
                           ItemsSource="{Binding Items}" IsStickyHeader="True" TapCommand="{Binding }"
                           SelectionMode="Multiple" IsStickyGroupHeader="True" GroupHeaderSize="50">

    <listView:SfListView.ItemTemplate>
        <DataTemplate>
            <Grid x:Name="grid" RowSpacing="1">
                <Grid.RowDefinitions>
                    <RowDefinition Height="*" />
                    <RowDefinition Height="*" />
                </Grid.RowDefinitions>
                <Grid.ColumnDefinitions>
                    <ColumnDefinition Width="50" />
                    <ColumnDefinition Width="*" />
                </Grid.ColumnDefinitions>

                <Image Margin="2,25,2,2" Source="{Binding ContactImage}" VerticalOptions="Center" HorizontalOptions="Center" HeightRequest="50"/>
                <Label Grid.Row="0"  Grid.Column="1" HorizontalTextAlignment="Center" HorizontalOptions="StartAndExpand" LineBreakMode="NoWrap" Text="{Binding ContactName}" FontSize="Medium" />
                <Label Grid.Row="1" Grid.Column="1" HorizontalTextAlignment="Center" HorizontalOptions="StartAndExpand" LineBreakMode="NoWrap" Text="{Binding ContactNumber}" FontSize="Small" />

            </Grid>
        </DataTemplate>
    </listView:SfListView.ItemTemplate>

</listView:SfListView>
```

## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
